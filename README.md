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

# Case study: Hipyo Tech

Hipyo Tech built a silent keyboard using the Velocifire Sun 68 keyboard kit [2]. The Sun 68 makes extensive use of gaskets, foams, and so on. The configuration is as follows, from the bottom up [3][4][5]:

* Silicone gaskets on the bottom case's screw holes.
* Two poron pads between the bottom case and the PCB.
* Silicone gaskets on the front and back edges of the four corners of the top case and centered on the left and right sides of the top case.
* Poron gaskets all along the top and bottom of the front and back edges of the polycarbonate plate.
* Washers/shims under the stabilizers. Material unknown.
* (Presumably brass) standoffs between the PCB and plate, secured with screws.
* Thin EVA film between the PCB and switches.
* Poron pad between the PCB and the plate.

The keyboard's sound varies dramatically depending on the switches. [4] and [5] demonstrate louder switches with tuned sound profiles. For a silent keyboard, choose silent switches, clearly.

Hipyo used Gazzew Boba Gum switches with heavy lube (Krytox 205 G0) for nearly silent operation. These have dampening pads that look like silicone or a similar material on the bottoms of the rails [2]. He strongly dislikes the feel of silent switches in general, perhaps because of the dampened bottom-out. He also chose 50 g springs so that he could type with less force and thus generate less noise.

## Lessons learned

Gasket mounting and foam do not, on their own, silence otherwise loud switches, at least as used in the Sun 68. It's unclear whether gasket mounting or other tricks are needed to further silence already quiet switches. Regardless, others in the community affirm that gasket mounting does alter the sound of the keyboard significantly [6].

Silent switches appear to be very quiet, as advertised, but might also feel very unpleasant to use. There might be a hard tradeoff between silent operation and a pleasant typing experience; if so, I will need to find the right balance for my own preferences. More case studies might help clarify this.

A lighter typing style, aided by lighter switches, will also yield a quieter typing experience overall.

Moderate to heavy lube might also contribute to quiet switch operation.

I will definitely need to test silent switches in person before committing to a choice.

# Case study: IO Sam

IO Sam built a silent keyboard using the Glorious GMMK TKL case and Zeal PC Aqua Zilent switches, aiming for a budget of around $250 [7]. He discussed the subject of silent keyboards in depth and detailed the process for building his budget silent keyboard. Like Hipyo Tech, IO Sam's keyboard was very quiet. Unlike Hipyo, IO Sam had no complaints about the feel of his switches.

He explicitly confirmed what I observed from Hipyo Tech's video and other builds using the same case as Hipyo: "Your choice of switches is the number one factor that will define the sound levels and characteristics of your board. Period. I don't care how fancy your keyboard case is and what kind of plate mounting mechanism it uses, the switch is ultimately *the* thing that will determine the noise level coming out of your board."

IO Sam gave a priority list for building a quiet keyboard:

1. **Switches:** silent switches make a silent keyboard. He used Zeal PC Aqua Zilents, with 67 g springs. He recommended a source for an in-depth review [8]. IO Sam considered these particular switches to be among the best on the market.
2. **Lube:** Krytox 205 G0.
3. **Keycaps:** PBT keycaps with thick walls for quieter, lower-pitched sound. His keycaps were 1.25mm thick.
4. **Stabilizers:** rattling stabilizers are key causes of disruptive noise in many/most keyboards. He used GMK Cherry-style plate-mounted stabilizers, but I presume I will use screw-in PCB-mounted ones in my build for strength and to reduce the chance of noise from rattling feet. Note that he had to clip all four feet on his stabilizers to eliminate unwanted noise.
5. **Damping foam:** buy a sorbothane sheet and cut it to fit between the bottom case and the PCB to prevent the case from echoing and amplifying sound. In general, dense foams work best for sound damping, and he recommends sorbothane as what many enthusiasts consider best-in-class.
6. **Case and PCB:** his comments focused on budgetary concerns rather than sound damping. He recommended that first-time builders use a hot swap PCB.

# Product selection

## Budget

No set budget. I'll spend what it takes to build my ideal keyboard, but I won't spend money for status symbols like scalper-priced keycaps.

## Form factor

I'm used to full-size keyboards with media keys and ~6 macro keys, but I'm starting to consider 60% layouts for the same reasons I love Vim, e.g. keeping my fingers on the home row. I'm fairly uncomfortable with the idea of ditching all of the other keys, but hopefully I can get hands-on time with some 60% keyboards and try them out locally. 

In fact, editing this document with GitHub's default editor leaves me wishing I could use Vim keys on a keyboard layer instead of arrow keys, Home, End, etc.

Of course, there's nothing stopping me from using the same, home-row-centric approach on a larger keyboard (e.g. 75%, TKL, or full-size). This approach is much friendlier for casual use or for use by others. Furthermore, it allows me to set a "default" layer that's fully stock and then, on other layers, use all those extra keys as dedicated macro keys.

If I'm fully comfortable with a 60% keyboard, I certainly do like the compactness, lightness, ergonomics, and so on that the layout offers.

One important unknown for me is whether I will still be able to press F keys, Delete, etc. to enter UEFI menus at boot.

## Case, PCB, plate

I don't yet have enough information to write about these. I'm initially inclined toward a stained and finished hardwood case, and obviously I want to make choices that deaden sound. I also want to keep the case reasonably light. I don't anticipate wanting weights, for instance.

I assume I will want hot swap sockets, since they seem so obviously convenient, but I don't know how durable they are. I don't own proper soldering equipment, so hot swap might save me quite a bit of money, not to mention time. Reliability and durability matter more to me, though, so I might wind up opting to solder my switches.

I don't know exactly what layout I want in terms of details like shift key size. KristoferYee's beginners guide suggests 2.25u as a default [1]. I want what I've always considered "standard" in my own experience; I will learn precisely how to specify this and update this section. I will ensure that the PCB, plate, and keycap set all match. The layout will be US QWERTY.

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

KristoferYee's beginners guide recommends screw-in stabilizers and recommends against snap-in stabilizers because the latter can easily snap out of place [1]. This sounds like good advice to me.

## Keycaps

From what I have heard, I presume I will either want PBT double-shot for backlit legends (which I thoroughly enjoy on my current keyboard as well as my laptop) or single-shot PBT with dye-sub legends. In the latter case, I might want fully custom legends that document my layers. If possible, I might also want to mix backlit and dye-sub legends in some way.

I have absolutely no idea what keycap profiles I want.

I don't think I like pudding keycaps.

I'm wary of over-customizing keycaps (e.g. by custom-printing legends). I know my keyboard layers are likely to change over time, and I don't want to face the choice between replacing my keycaps due to (potentially minor) changes in my layer configuration and having keycaps that don't reflect the keys' actual functions. I'm not sure how I will resolve this. It's conceivable that I might write my own secondary labels in pen (maybe in architectural script) and use a solvent like acetone to remove and replace them when needed; there might be other creative options as well.

## Cables

I have no specific products or vendors in mind, yet. I prefer straight cables over coiled cables.

## Batteries

Ideally, I would love to be able to power the keyboard with rechargeable Lithium standard cells, but I don't know much about them (yet) and don't know how viable this is. The battery **must** be fully replaceable and standard so that I can be confident that I'll be able to replace it for at least 10 years.

# Resources

Marketplace: [kbdfans.com](https://kbdfans.com)

Marketplace: [Drop](https://drop.com/)

Marketplace: [KeebsForAll](https://keebsforall.com/)

Marketplace: [1up Keyboards](https://1upkeyboards.com/)

Community forum & secondhand market: [r/MechanicalKeyboards](https://www.reddit.com/r/MechanicalKeyboards/)

Community forum: [geekhack.org](https://geekhack.org/)

# Sources

[1] KristoferYee (YouTube): [*The Worst Hobby on the Internet - Mechanical Keyboards (Beginners Guide)*](https://www.youtube.com/watch?v=xzWm40Tq4F4)

[2] Hipyo Tech (YouTube): [*The worlds most SILENT keyboard.🔇*](https://www.youtube.com/watch?v=Q9k0YkiwgUk)

[3] Velocifire: [*[Extra] Sun68 Gasket Keyboard Kit*](https://www.velocifiretech.com/collections/sun-68/products/fyf?variant=39749347967094)

[4] bored bear (YouTube): [*Sun68 Prototype Custom Keyboard Build & Typing Sounds | E-yellow with H1 switches and BoW Keycaps*](https://www.youtube.com/watch?v=lpkNIH2AKL8)

[5] Keyeah (YouTube): [*Sun68(CN ver) Unboxing & Build | Glacier Panda Switches*](https://www.youtube.com/watch?v=Tsip9_p4vog)

[6] GeekHack: [*Topic: What is a gasket mounted keyboard?*](https://geekhack.org/index.php?topic=101731.0)

[7] IO Sam (YouTube): [*How to build a whisper quiet mechanical keyboard (modded GMMK + Aqua Zilents + Matrix Keycaps)*](https://www.youtube.com/watch?v=3s4ruFFqmqo)

[8] uploadTwashe (YouTube): [*The Zilent 67g Switch Review - ZealPC - I like these more than Holy Pandas!*](https://www.youtube.com/watch?v=JKtF9nB-3BU)
