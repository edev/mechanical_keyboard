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
2. **Lube:** Krytox 205 G0 and Permatex Dielectric Tune-Up Grease.
3. **Keycaps:** PBT keycaps with thick walls for quieter, lower-pitched sound. His keycaps were 1.25mm thick, but he acknowledges that more premium options are thicker and that these might be superior.
4. **Stabilizers:** rattling stabilizers are key causes of disruptive noise in many/most keyboards. He used GMK Cherry-style plate-mounted stabilizers, but I presume I will use screw-in PCB-mounted ones in my build for strength and to reduce the chance of noise from rattling feet. Note that he had to clip all four feet on his stabilizers to eliminate unwanted noise.
5. **Damping foam:** buy a sorbothane sheet and cut it to fit between the bottom case and the PCB to prevent the case from echoing and amplifying sound. In general, dense foams work best for sound damping, and he recommends sorbothane as what many enthusiasts consider best-in-class. He used a sorbothane with a hardness of 50 Duro.
6. **Case and PCB:** his comments focused on budgetary concerns rather than sound damping. He recommended that first-time builders use a hot swap PCB. PCBs that support PCB-mounted, screw-in stabilizers are best. He chose the GMMK because of its TLK size (per his preference), aluminum plate for rigidity, hot swap sockets, decent looks, and relatively easy modding. This is not the case for me, for many reasons, starting with software customization limitations.

He provided a tool list as well:

* A large, well-lit workspace.
* Soldering iron (unless using hot swap sockets).
* Utility knife or X-Acto knife for cutting damping foam to size.
* Switch opener. The most popular 3, he said, were:
  * MechanicalKeyboards.com MX Switch Top Removal Tool. Works best on soldered, plateless switches. Not recommended for use on loose switches.
  * KBDfans X ai03 2-in-1 Aluminum Switch Opener. His personal favorite, since it opens both Cherry/Gateron and Kailh switches.
  * KiiBoss Aluminum MX kiiOpener. Many find it more ergonomic than the KBDfans model because it's taller.
* Fine nylon brushes for lubing switches and stabilizers. He recommended any generic acrylic, oil, or watercolor paintbrush set that includes small-gauge liner brushes. He used #2 for lubing switches and #6 for lubing stabilizers.
* Precision screwdrivers.
* Long-nose pliers.
* Precision tweezers.
* Jeweler pick-up tool.
* Flush cutter for clipping stabilizer and switch legs. Only needed if there's a mismatch between the PCB and the switches or if the stabilizers tick and need modding.
* Eye protection when clipping stabilizer and switch legs!
* Metal ruler and optional caliper for cutting foam to size.
* Cutting mat for cutting foam to size.
* Optional magnifier lamp.
* Cotton swabs and isopropyl alcohol for cleaning up lube.
* Optional switch modding station (AKA lube station).
* Bandages and a glue stick, if performing the Band-Aid stabilizer mod.

IO Sam walked through his build process. (In the list below, I omit details that are irrelevant for my own build.) His procedure was as follows:

1. Lube the switches. "The first thing to note here is that I went for a thicker lube coating, since these Zilents switches have a very sharp tactility and would not become numb if they were lubed generously. The goal here is to completely drown any hint of ping noise or scratchiness out of the switches as much as possible and go for a buttery, Topre-like sound for this board." For an introduction to lubing switches, he recommended another YouTuber's guide [9].

    * Bottom housing: rails (generously), inside of barrel/well, and floor.
    * Stem spring: lube thoroughly on all sides. (Note: Hipyo Tech generally uses the much faster plastic bag method.)
    * Stem: all four walls plus center shaft.
    * Top housing: all four rails.

2. Clip the switches' extra legs, if needed. He explained that some switches are "PCB-style" switches: they include two extra, plastic legs on the bottom to help stabilize them during soldering. "Plate-style" switches instead have clips on the sides to secure into the plate for stability and lack these extra legs. Some hot swap PCBs omit the holes for these extra legs. Thus, if I choose a PCB without these extra holes (i.e. with 3 holes instead of 5) and PCB-style switches with these legs, I will need to use flush cutters to trim these two, extra plastic legs.

3. Test all of the switch contacts using keyboard-testing software. Bridge the switches' contacts with tweezers and verify that the computer registers keypresses.

4. Mod the stabilizers. He removed the original, plate-mounted stabilizers, discarded them, and cleaned the factory lube from the plate with rubbing alcohol and cotton swaps. He disassembled his new stabilizers and modified them as follows:

    * Outer housings: lube the inside walls with Krytox.
    * Stems: clip all four legs. Lube all four sides with Krytox.
    * Wires: lube the corners, where they snap into the outer housings, with Krytox. Lube the ends with Permatex.
    * PCB: Band-Aid mod. Specifically, cut out strips of standard, small bandages; glue them to the PCB where the stabilizer stems will impact; and spread Permatex on top of them to further absorb sound when the stabilizer stems come down.

    It's unclear to me from the video whether either the Band-Aid mod or clipping the stabilizer stems is necessary on the PCB-mounted, screw-in stabilizers I hope to use for my own keyboard. I will need to research this further.

5. Install sorbothane in the bottom case. Cut it to fit and install it. Leave the outer plastic on until the end, since sorbothane is very sticky.
 
    After observing this, I wonder if it might be helpful to apply a layer of fabric or foam over the top of the sorbothane to prevent it from accumulating a permanent layer of dust or sticking to the PCB. IO Sam re-applied the thin, stock foam sheet from the GMMK atop the sorbothane to resolve this issue.
   
    It's also clearly important to understand the geometry of the bottom case and the height of the cavity underneath the PCB to choose the most appropriate thickness of sorbothane sheet: he spent a lot of time cutting out individual strips of sorbothane to fit into the spaces between the bottom case's ribs, when he might have been able to simply cut a single rectangle and then cut out holes for the standoffs if the sorbothane had been a couple millimeters thinner.
   
6. Assemble the keyboard.

7. Test keys and stabilizers for proper function and noise; fix any issues, e.g. by re-applying lube.

    To further silence stabilizers, he referred to another YouTuber's video detailing a technique for installing O rings on the stabilizer wires [10]. He found this to be unnecessary on his keyboard.

## Lessons learned

This comprehensive build video provides high-quality reference material for many of the tools, techniques, and parts I'll need to build my own, silent keyboard. I will research other people's views on many of the techniques and products he chose, and I may adopt them for my own build.

This video introduced me to and taught me about two, particularly important topics: sorbothane and lubing for silence. I will carry these lessons forward.

Compared to Hipyo, IO Sam also appeared to choose much higher quality switches, and he appeared to like them much more than Hipyo as well. If others in the space agree about these Zilent switches, and if there are no further evolutions in switch design in the nearly two years since IO Sam published his video, I may use these switches as well.

Gasket mounting is clearly optional for silent builds. I will need to evaluate this further before making final choices, unless I find a case kit that fits my use case perfectly and effectively makes this choice for me.

# Product selection

## Budget

No set budget. I'll spend what it takes to build my ideal keyboard, but I won't spend money for status symbols like scalper-priced keycaps.

## Form factor

I'm used to full-size keyboards with media keys and ~6 macro keys. I'm willing to consider smaller keyboards, but I'm hesitant. My thoughts on some common 60% keyboard arguments are as follows:

1. *60% keyboards are better for producitivity because your keyboard's layers bring the keys to you, just like Vim, rather than requiring your fingers to travel far and wide.* I like this productivity-based argument, and, yes, this is one of the reasons I love Vim, too. However, I can achieve these exact same effects on the 60% portion of any larger keyboard as well! At its heart, this is an argument in favor of a layered keymap, not a smaller keyboard. I am thoroughly convinced that I want to try using a layered keymap on whatever keyboard I choose.

2. *60% keyboards are more egonomic for gaming because all that extra width pushes your mouse hand to the right.* This argument holds very little weight for me, given my wide frame and long arms. I admit that I might change my mind after trying it for a while, but I'm strongly disinclined to make a radical change to my keyboard form factor based on an ergonomics argument that doesn't resonate with my own experiences.

3. *60% keyboards are small and compact, so they'll improve the look and feel of your workspace.* I have always liked the size of my keyboard; this argument carries no weight for me at all.

A larger keyboard will be much friendlier for casual use, since most or all keys will be available without needing to resort to layers. It will also be much easier for friends to use or borrow: a tiny keyboard would be uncomfortable or even unusable for a guest! Furthermore, it allows me to set a "default" layer that's fully stock and then, on other layers, use all those extra keys as dedicated macro keys.

I'm willing to try a tenkeyless (TKL) layout. This seems to me like the ideal resolution to all of my priorites and concerns above, and I like the look of it, too. It preserves the exact layout I have known and liked my whole life. I might miss the numpad a bit, but I can touch type the entire 60% portion of my keyboard comfortably and at speed, so it will probably just push me to further hone my numeric-symbolic typing. I can always add a standalone numpad later if I want one. Besides, I've adjusted just fine to a tenkeyless laptop over the last few years.

If I have an 80%-or-larger keyboard, e.g. TKL, 1800, or full-size, and I'm looking for a second keyboard, I'll be much more inclined to consider a more radical departure from full-size QWERTY. There are very interesting 60%, ergonomic, split, and ortholinear keyboard kits made for ZMK, for instance. A 60% keyboard running ZMK might be a great travel (or backpack) keyboard, especially given that the battery might last in the ballpark of six months. I intend for my first custom keyboard to be TKL, though.

## Case, PCB, plate

**[Case]** I'm aware that I will probably want to swap my keycaps periodically, probably mostly for aesthetic reasons. Thus, I want my case to act as a neutral base. While I love the look of hardwood, I think black or dark gray is a much more generally useful colorway for this purpose.

Since I tend to move my keyboards around quite a lot, I want to optimize my case for this: rounded edges for safety, easy-to-grip material, and moderate to light weight. For these reasons as well as to allow Bluetooth operation, plastic seems to be ideal.

While I rarely use them, I want my case to include fold-out feet. I simply can't imagine going to all the effort and expense of building this keyboard while lacking such a basic ergonomic and quality-of-life feature.

**[PCB]** I assume I will want hot swap sockets, since they seem so obviously convenient, but I don't know how durable they are. I don't own proper soldering equipment, so hot swap might save me quite a bit of money, not to mention time. Reliability and durability matter more to me, though, so I might wind up opting to solder my switches in the long run. Even if I do that, it might still be useful to have a hot swap board on hand so I can experiment quickly and easily, if I find myself building multiple keyboards. Therefore, I tentatively choose hot swap for this build.

**[Plate]** I have no strong preferences, though this might change in time. I simply don't yet know what I like.

**[Keychron K8 Pro]** The [Barebone kit](https://www.keychron.com/products/keychron-k8-pro-qmk-via-wireless-mechanical-keyboard?variant=39755425972313) seems to fit all of these requirements very well.

## Layout

I don't know exactly what layout I want in terms of details like shift key size. KristoferYee's beginners guide suggests 2.25u as a default [1]. I want what I've always considered "standard" in my own experience; I will learn precisely how to specify this and update this section. I will ensure that the PCB, plate, and keycap set all match. The layout will be US QWERTY.

## Controller

I'm aware of AVR and ARM options, broadly speaking, and I believe AVR is nearing end of life in terms of firmware support due to hardware limitations. I presume I want ARM, but I don't have a specific controller or board in mind, yet.

## Firmware

**[QMK]** My understanding so far is that QMK is the typical go-to for most enthusiasts. I've spent an hour or so browsing the docs, and I like what I see. I'm under the impression that it may be difficult or impossible to build a wireless keyboard with QMK due to closed source Bluetooth firmware. I understand and respect the principled stance of GPL-licensed firmware. At the same time, wireless connectivity is a hard requirement for me, so I don't know if QMK will work for my use case.

**[ZMK]** I understand that ZMK specifically uses an MIT license to allow the use of such closed source firmware packages and supports Bluetooth on some controllers out of the box as a result. I may opt for ZMK because of this. I haven't spent much time reading ZMK's docs.

**[TMK]** My understanding is that QMK forked from TMK and that most in the community have chosen QMK. While I respect TMK, I initially choose to follow the wisdom of the pack, unless information comes to light that indicates TMK would be the better choice for my use case.

At this time, either QMK or ZMK might be a great fit for my everyday needs. ZMK's more mordern architecture and, in particular, its exceptional battery life argue persuasively in favor of ZMK. However, after reviewing all hardware listed on the ZMK docs, I haven't seen a single product that fits my other needs, particularly a TKL form factor [11]. Therefore, ZMK seems like a dead end for this particular keyboard build.

Meanwhile, the [Keychron K8 Pro Barebone kit](https://www.keychron.com/products/keychron-k8-pro-qmk-via-wireless-mechanical-keyboard?variant=39755425972313) provides QMK and Bluetooth 5.1 support simultaneously, apparently by using a separate Bluetooth chip [12]. I'm guessing that this approach is far from technically ideal, but I have heard no complaints from reviewers or users, and the keyboard switches to 1000 Hz polling when connected by USB-C. I find this quite compelling.

## Switches

[Zeal's Zilent V2 (Silent Tactile)](https://zealpc.net/products/zilent?variant=5894817710118) seem to be widely regarded as either the best or among the best silent tactile switches, and Zeal seems to have a reputation for excellence in general. I'm tentatively choosing these switches, but I'll try the [Zeal Switch Sampler Pack](https://zealpc.net/products/zeal-switch-sampler-pack?variant=13152556613695) switch tester to confirm that I like them before buying a full set.

## Stabilizers

KristoferYee's beginners guide recommends screw-in stabilizers and recommends against snap-in stabilizers because the latter can easily snap out of place [1]. This sounds like good advice to me.

My general sense from others in the community is that [Zeal's screw-in stabilizers](https://zealpc.net/products/zealstabilizers?variant=27196398790) are pretty much the best around. Most commonly, I hear builders saying they're choosing cheaper stabilizers that they find to be almost as good as Zeal's. I suspect I will need to lube them and Band-Aid mod them as IO Sam laid out, though I don't know for sure [7].

I consistently hear that Durock stabilizers are very good as well; Hipyo Tech and others commonly recommend them as their go-to stabilizers. I'll keep them in mind, but I'm tentatively choosing Zeal's screw-in stabilizers.

## Keycaps

From what I have heard, I presume I will either want PBT double-shot for backlit legends (which I thoroughly enjoy on my current keyboard as well as my laptop) or single-shot PBT with dye-sub legends. In the latter case, I might want fully custom legends that document my layers. If possible, I might also want to mix backlit and dye-sub legends in some way.

I have absolutely no idea what keycap profiles I want.

I don't think I like pudding keycaps.

I'm wary of over-customizing keycaps (e.g. by custom-printing legends). I know my keyboard layers are likely to change over time, and I don't want to face the choice between replacing my keycaps due to (potentially minor) changes in my layer configuration and having keycaps that don't reflect the keys' actual functions. I'm not sure how I will resolve this. It's conceivable that I might write my own secondary labels in pen (maybe in architectural script) and use a solvent like acetone to remove and replace them when needed; there might be other creative options as well.

## Cables

I have no specific products or vendors in mind, yet. I prefer straight cables over coiled cables.

## Batteries

After talking with a friend and examining various ZMK boards and shields, it seems they're commonly built to work with standard, rechargeable, 3.7V Lithium batteries [11]. If I wind up building a keyboard that requires me to provide my own battery, I'm inclined to consider a standardized form factor like 18650. I will investigate form factors if and when the times comes.

My general strategy is simple: since the battery is the primary wear part on almost any battery-containing device, I intend to ensure that whatever battery I use is fully replaceable and standard so that I can be confident that I'll be able to replace it for at least 10 years.

# Keychron K8 Pro

The [Keychron K8 Pro Barebone kit](https://www.keychron.com/products/keychron-k8-pro-qmk-via-wireless-mechanical-keyboard?variant=39755425972313) seems to be ideal for my needs at this stage. It provides an easy entry point for my first custom keyboard, and it checks all of my boxes quite well, as far as I know. I might eventually move on to a much more involved ZMK build; if so, I'm confident that my experience building the K8 Pro will prepare me well for a more advanced follow-up project.

To complete the build, all I will need are switches, keycaps, and stabilizers, plus modding and building tools. The K8 Pro includes a case and plate that I believe will work well for me, and it even includes high-quality sound damping very close to what IO Sam recommended in his build [7].

Before committing to this, I will want to investigate potential issues, including:

1. Battery replacement: buying a replacement, removing the original battery, installing the new one, informing the firmware (if needed), etc.
2. Precise key layout, including shift key sizes, etc.
3. Watch many more reviews in case I've missed other problems or issues.

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

[9] Joe Gaz (YouTube): [*How to Lube Mechanical Keyboard Switches! (Detailed)*](https://www.youtube.com/watch?v=-GkZpD58dFk)

[10] Mike Walker (YouTube): [*Silencing stabs the Walker way*](https://www.youtube.com/watch?v=9pCilf3h7O4)

[11] ZMK: [*Supported Hardware | ZMK Firmware*](https://zmk.dev/docs/hardware)

[12] u/UJL123 (Reddit): [*How does keychron K8 pro support both QMK and bluetooth?*](https://www.reddit.com/r/olkb/comments/u2e9z5/how_does_keychron_k8_pro_support_both_qmk_and/)
