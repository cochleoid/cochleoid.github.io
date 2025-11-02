---
title: "Screenshotting in DWM with Scrot (and OCR with Tesseract)"
date: 2025-10-31
draft: false
description: "A concise tutorial on adding screenshot and OCR support in dwm using Scrot and Tesseract."
tags: ["linux", "dwm", "screenshot"]
---

## **Introduction**

I personally use dwm by suckless as my window manager of choice for its sheer simplicity. Sure, AwesomeWM may have the cool rice, but I like to keep my setup concise and easy to debug if a nasty error lurks. Sometimes, I just wanna share this setup with others, but wait, how *can* you screenshot in this barren wasteland? Just look at that void: not a screenshot button in sight. But wait again… how was the screenshot below even taken?

![DWM Screenshot](DWMScreenie.png)

---

## **Finding Source**

Let’s head to the source code to try to solve this mystery. Head over to your build directory, which in my case was `/usr/src/dwm/` and open our config file where the commands are. Goodness, what does any of the below mean!

```c
/* commands */

static char dmenumon[2] = "0"; /* component of dmenucmd, manipulated in spawn() */
static const char *dmenucmd[] = { "dmenu_run", "-m", dmenumon, "-fn", dmenufont, "-nb", col_gray1, "-nf", col_gray3, "-sb", col_cyan, "-sf", col_gray4, NULL };
static const char *lichess[]  = { "/usr/bin/librewolf", "--new-window", "lichess.org", NULL };

static const Key keys[] = {
	/* modifier                    key        function        argument */
	{ MODKEY,                      XK_p,      spawn,          {.v = dmenucmd } },
	{ MODKEY|ShiftMask,            XK_Return, spawn,          {.v = termcmd } },
```

We’re looking dead straight at an array in C. Looking at the basic format, we can see that for every “key,” there’s an associated keybind and argument. As we will see below, an argument is simply the binary or command being run. If we need a screenshot command, we will have to choose a worthy screenshotting application first.

---

## **Scrot!**

For screenshotting, I suggest the modular Scrot binary for most people. It does exactly what you need to do, with a variety of parameters that could save screenshots to whichever directory you may need (`~/Pictures` comes to mind…)

For those new to package browsing (or too lazy, if I were the reader): I’ve provided the install commands for the major distros. Sorry, Hannah Montana Linux, maybe next time.

**Ubuntu/Debian**
```bash
sudo apt-get install scrot
```

**Arch-Based**
```bash
sudo pacman -S scrot
```

**Fedora**
```bash
sudo yum install scrot
```

**OpenSUSE**
```bash
sudo zypper install scrot
```

---

## **Adding Scrot to Commands**

Now that you’ve actually got a screenshotting utility installed, let’s look at how we can add it into the array.

For the commands section, we’re gonna need the binary and some parameters. Scrot is pretty handy in that it’s got loads of options with how you want the screenshot to come out. As for me, I like to select a region to screenshot (the “-s” parameter), and having that screenshot directly funneled into the home directory:

```c
static const char *scrot[] = { "scrot", "-s", "Screenshot.png", NULL };
```

For those who want a dedicated folder, you can tack it on to the directory. If you prefer a whole-screen capture or if you want a separate command for it, you can make this quick change:

```c
static const char *scrot[] = { "scrot", "Screenshot.png", NULL };
```

---

## **Adding a Keybind**

Fast forward a bit to the keybind section, we can finally add the keyboard shortcut to call Scrot. We can simply append the below, where `MODKEY|ShiftMask` and `XK_s` would imply the shortcut **ALT+SHIFT+S**.

```c
{ MODKEY|ShiftMask,             XK_s,      spawn,      {.v = scrot } },
```

---

## **Bonus: Piping into OCR**

As a cool bonus, we can also pipe Scrot into an OCR tool to get immediate OCR scans into our clipboard after selecting an on-screen region. We can write a quick bash file titled `ocrcapture` for this task in `/usr/bin`:

```bash
#!/bin/bash
scrot -s /tmp/ocr.png
tesseract /tmp/ocr.png stdout | xclip -selection clipboard
rm -f /tmp/ocr.png
```

And of course, here is the dwm config implementation:

```c
static const char *ocrcapture[]  = { "/usr/bin/ocrcapture", NULL };
{ MODKEY|ShiftMask,             XK_y,      spawn,      {.v = ocrcapture } },
```

---

## **Conclusion**

In this brief tutorial, we enabled screenshotting and OCR scanning in dwm through just a few keyboard clicks (and a little bash). Imagine my satisfaction being able to add in screenshotting to the dwm keybinds after months of just manually typing in the scrot commands in CLI each time. I hope that same satisfaction is one I can lend to you.
