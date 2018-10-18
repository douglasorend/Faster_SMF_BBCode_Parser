[hr]
[center][color=red][size=16pt][b]FASTER SMF PARSER v2.0[/b][/size][/color]
[url=http://www.simplemachines.org/community/index.php?action=profile;u=253913][b]By Dougiefresh[/b][/url] -> [url=http://custom.simplemachines.org/mods/index.php?mod=4069]Link to Mod[/url]
[/center]
[hr]

[color=blue][b][size=12pt][u]Introduction[/u][/size][/b][/color]
The SMF parser in the SMF 2.0.x line, as well as the SMF 2.1 Beta 1 & 2, have a potentially "fatal flaw", at least where it concerns bbcodes with a large number of parameters.  The original SMF code generates permutations of all possible combinations of the parameters in order to make it easier for the user to use bbcodes, and then checks to see which permutation is the right one.  A bbcode with 14 parameters generates 98,306 permutations, taking little more than half a second on my system [b]PER USE[/b] and using [b]90MB[/b] of memory!!  Checking for 15 parameters crashes my forum with an out-of-memory error because it attempts to allocate more than 128MB of memory!

SMF 2.1 Beta 3 takes a different approach to the "fatal flaw", avoiding the use of a permutation array prior to processing the parameter permutations.  This avoids the possible of a forum crash, plus potentially allows for more parameters to be processed without having to rearrange parameters.

Please note that both this mod and SMF 2.1 Beta 3 function in place, as other mods or future forum versions may need the built-in functionality.

[color=blue][b][size=12pt][u]Related Discussion[/u][/size][/b][/color]
o [url=http://www.simplemachines.org/community/index.php?topic=538611.msg3827580#msg3827580]REPORT: Potentially "Fatal Flaw" in SMF's bbcode parser[/url]

[color=blue][b][size=12pt][u]Admin Settings[/u][/size][/b][/color]
There are no admin settings to this mod.  To disable, you must uninstall this mod.

[color=blue][b][size=12pt][u]Compatibility Notes[/u][/size][/b][/color]
This mod was tested on SMF 2.0.14, but should work on SMF 2.0 and up.  SMF 1.x is not and will not be supported.

[color=blue][b][size=12pt][u]Changelog[/u][/size][/b][/color]
The changelog has been removed and can be seen at [url=http://www.xptsp.com/board/index.php?topic=580.msg896#msg896]XPtsp.com[/url].

[color=blue][b][size=12pt][u]License[/u][/size][/b][/color]
Copy of SMF 2.1 Beta 3's License as copied from the [b]LICENSE[/b] file in that install:
[quote]Copyright © 2011 Simple Machines. All rights reserved.

Developed by: Simple Machines Forum Project
Simple Machines
http://www.simplemachines.org

All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of SMF2.1 nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
[/quote]