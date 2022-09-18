# Mechanical Keyboard

Building a custom mechanical keyboard involves a great deal of research and planning. This repository maps out the problem space with a focus on the keyboard I may eventually build for myself. If you're reading this, welcome, and I hope it helps you on your journey! Constructive contributions of all kinds are welcome: please open an Issue or pull request, and thanks in advance!

# User story

* I'm constantly writing both software and English, both personally and professionally. These are my primary, motivating use cases; everything else is secondary.
* I own at least 3 off-the-shelf keyboards other folks can use when they come over, so I'm okay with customizing my keyboard to suit my exact use case.
* I love Linux and Vim, and I use them constantly. I use Windows daily, too. I never use Macs, and I don't plan to start.
* I play games sometimes, and when I do, I use macros a fair bit. I tend to play the same games for weeks or months rather than hopping between games, so I can tolerate a little bit of hassle in setting up a new profile, if the end result is worth the effort. On-the-fly customization (from Windows, while gaming) is a nice-to-have, not a must-have.
* I use my keyboard from my desk, from my couch, and sometimes from the kitchen. My ideal keyboard can go anywhere I go and talk to whatever computers are nearby.
* I most often work from home, but I occasionally co-work with a friend, and I may work in an office at least some of the time in the future. If my keyboard is noticeably audible to those around me, I won't be comfortable using it.
* I often use my keyboard and a microphone simultaneously, e.g. for gaming with friends or conferencing. I want to be able to use any microphone that's convenient without broadcasting keyboard noise.
* I often listen to quiet, instrumental music while I work. I don't want my keyboard to disturb it.
* I want my next keyboard to last me a long time, both in terms of meeting my needs and in terms of being fully serviceable and supported by firmware updates for a long time.
* I sometimes control 2-3 computers on my desk in a single session, e.g. desktop, laptop, and home server.

# Wish list

* Silent operation.
* Tactile switches.
* Maximally powerful firmware customization.
* Full functionality and customization on Linux, full or nearly full on Windows.
* Secure, encrypted wireless operation via Bluetooth. A dongle option would also be great, but I know it might not happen.
* Wired operation via detachable USB-C. Multiple USB-C connections would be great, but I know it might not happen.
* Input switching between USB-C and wireless, preferably via programmable key combos.
* N-key rollover.
* Full, long-term serviceability, i.e. the ability to replace or upgrade every single part, for at least 10 years.
* Long-term firmware support, i.e. at least 10 years of expected support for the controller.
* Per-key RGB backlighting.
* Warm, elegant, timeless aesthetic. I have no interest in what's fashionable at any moment in time.
* Rounded case corners, light weight, and other design choices for comfortable everyday use and transportation.

Things I explicitly do not want:

* Wireless charging (of any kind, in any direction)
* USB passthrough or hub
* Audio

# Product selection

## Budget

No set budget. I'll spend what it takes to build my ideal keyboard, but I won't spend money for status symbols like scalper-priced keycaps.

## Form factor

I'm used to full-sized keyboards with media keys and ~6 macro keys, but I'm starting to consider 60% layouts for the same reasons I love Vim, i.e. keeping my fingers on the home row. I'm fairly uncomfortable with the idea of ditching all of the other keys, but hopefully I can get hands-on time with some 60% keyboards and try them out locally.

In fact, editing this document with GitHub's default editor leaves me wishing I could use Vim keys on a keyboard layer instead of arrow keys, Home, End, etc.

If I'm fully comfortable with a 60% keyboard, I certainly do like the compactness, lightness, ergonomics, and so on that the layout offers.

One important unknown for me is whether I will still be able to press F keys, Delete, etc. to enter UEFI menus at boot.

## Case, PCB, plate

I don't yet have enough information to write about these. I'm initially inclined toward a stained and finished hardwood case, and obviously I want to make choices that deaden sound. I also want to keep the case reasonably light. I don't anticipate wanting weights, for instance.

I assume I will want hot swap sockets, since they seem so obviously convenient, but I don't know how durable they are. I don't own proper soldering equipment, so hot swap might save me quite a bit of money, not to mention time. Reliability and durability matter more to me, though, so I might wind up opting to solder my switches.

## Controller

I'm aware of AVR and ARM options, broadly speaking, and I believe AVR is nearing end of life in terms of firmware support due to hardware limitations. I presume I want ARM, but I don't have a specific controller or board in mind, yet.

## Firmware

**[QMK]** My understanding so far is that QMK is the typical go-to for most enthusiasts. I've spent an hour or so browsing the docs, and I like what I see. I'm under the impression that it may be difficult or impossible to build a wireless keyboard with QMK due to closed source Bluetooth firmware. I understand and respect the principled stance of GPL-licensed firmware. At the same time, wireless connectivity is a hard requirement for me, so I don't know if QMK will work for my use case.

**[ZMK]** I understand that ZMK specifically uses an MIT license to allow the use of such closed source firmware packages and supports Bluetooth on some controllers out of the box as a result. I may opt for ZMK because of this. I haven't spent much time reading ZMK's docs.

**[TMK]** My understanding is that QMK forked from TMK and that most in the community have chosen QMK. While I respect TMK, I initially choose to follow the wisdom of the pack, unless information comes to light that indicates TMK would be the better choice for my use case.

## Switches

I don't know, yet.

## Stabilizers

I don't know, yet. People seem to swear by Durock, but I need to do a lot more research.

## Keycaps

From what I have heard, I presume I will either want PBT double-shot for backlit legends (which I thoroughly enjoy on my current keyboard as well as my laptop) or single-shot PBT with dye-sub legends. In the latter case, I might want fully custom legends that document my layers. If possible, I might also want to mix backlit and dye-sub legends in some way.

I have absolutely no idea what keycap profiles I want.

I don't think I like pudding keycaps.

I'm wary of over-customizing keycaps (e.g. by custom-printing legends). I know my keyboard layers are likely to change over time, and I don't want to face the choice between replacing my keycaps due to (potentially minor) changes in my layer configuration and having keycaps that don't reflect the keys' actual functions. I'm not sure how I will resolve this. It's conceivable that I might write my own secondary labels in pen (maybe in architectural script) and use a solvent like acetone to remove and replace them when needed; there might be other creative options as well.

## Cables

I have no specific products or vendors in mind, yet. I prefer straight cables over coiled cables.

## Batteries

Ideally, I would love to be able to power the keyboard with rechargeable Lithium standard cells, but I don't know much about them (yet) and don't know how viable this is. The battery **must** be fully replaceable and standard so that I can be confident that I'll be able to replace it for at least 10 years.
