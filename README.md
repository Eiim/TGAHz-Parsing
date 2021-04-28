# TGAHz Parsing

### What is this?

So, HzMod is a 3DS image capturing system that is entirely software-based. It can stream the 3DS top screen to a PC like NTR CFW. Development is a little strange... Archives of builds are hosted on this website: https://chainswordcs.com/horizon-by-sono.html

So, older builds (February 2018) can stream in a TARGA image format. The capability is available for all games I believe, but for some games it is required (such as Mario Kart 7, Super Smash Bros. for Nintendo 3DS, Yoshi's New Island, and Pokemon Yellow Version)

The TARGA image format streamed by HzMod is non-standard, so this repository is to document our reverse engineering efforts. Eventually we plan to push some changes to Snickerstream to add support to TARGA streams: https://github.com/RattletraPM/Snickerstream

# Key

* R = This bit is part of the Red
* G = This bit is part of the Green
* B = This bit is part of the Blue
* A = This bit is the 'Attribute Bit'

# Image Parsing Results

## Commit [139fa601fc96389fba8d3332ca6f058a16d84994](https://github.com/Eiim/TGAHz-Parsing/commit/139fa601fc96389fba8d3332ca6f058a16d84994)

https://cdn.discordapp.com/attachments/836413155894100050/837059467703091210/TGAHZ.png

Bit order: ARRRRRGG GGGBBBBB

![](https://cdn.discordapp.com/attachments/836413155894100050/837059467703091210/TGAHZ.png)

## Commit [387e2164f31f00570f211fb9b1e1fff9c635d218](https://github.com/Eiim/TGAHz-Parsing/commit/387e2164f31f00570f211fb9b1e1fff9c635d218)

https://cdn.discordapp.com/attachments/836413155894100050/837069486389198848/RRRRRRGG_GGGBBBBB.png

Bit order: RRRRRRGG GGGBBBBB

![](https://cdn.discordapp.com/attachments/836413155894100050/837069486389198848/RRRRRRGG_GGGBBBBB.png)

https://cdn.discordapp.com/attachments/836413155894100050/837069485445218364/RRRRRGGG_GGGBBBB.png

Bit order: RRRRRGGG GGGBBBBA

![](https://cdn.discordapp.com/attachments/836413155894100050/837069485445218364/RRRRRGGG_GGGBBBB.png)

https://cdn.discordapp.com/attachments/836413155894100050/837069483596185620/RRRRRGGG_GGBBBBBA.png

Bit order: RRRRRGGG GGBBBBBA

![](https://cdn.discordapp.com/attachments/836413155894100050/837069483596185620/RRRRRGGG_GGBBBBBA.png)

## Commit [4c910bf2f3f5fc08fdeacda75d5cde884d9f5a98](https://github.com/Eiim/TGAHz-Parsing/commit/4c910bf2f3f5fc08fdeacda75d5cde884d9f5a98)

https://cdn.discordapp.com/attachments/836413155894100050/837097268192346142/TGAHZ.png

![](https://cdn.discordapp.com/attachments/836413155894100050/837097268192346142/TGAHZ.png)

# Running the Script

Right now, the TGA image file and header information are hard-coded into the Python script.

This script is written in Python 3.
