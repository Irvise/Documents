# Introduction

The aim of this simple "guide" is to present most of the (best) software I have found that works on Linux, though most of them also run on other platforms. Oh, and they are all FSF approved (libre software if you don't know what FSF is). Try the software and give it a spin to see if it suites your needs. Also, here goes a disclaimer: I am by no means an expert in most of the software listed below, however, the time I have used has proven to be more than pleasant and productive; the only requirement I ask from the program in question is for it to be great for power users.

Also note that some programs may fit several categories listed below. I will list it were I feel it suites best.

## Table of Contents

* [Terminal applications](#terminal-applications)
* [Text editors](#text-editors)
* [Programming](#programming)
* [Web](#browsers---web)
* [Multimedia](#multimedia)
* [Document creation](#document-creation)
* [Office](#office-software)
* [Engineering, Science](#science---engineering)
* [Games](#games)
* [Other utilities](#miscellaneous)
* [Extras](#extras)
* [Programming languages](#programming-languages)
* [Social media](#social-media)
* [Project management](#project-management)

## Linux/BSD/Illumos distributions

### Stability wise

These distributions are mostly based on the premise of delivering a stable experience. However, this does not mean you are bounded to use only _stable_ software. Some distributions allow you to use newer software, such as Alpine (community repo), OpenSUSE (Tumbleweed), MX Linux (Debian backports and testing), NetBSD (current branch), FreeBSD (current branch).

* [Alpine Linux](https://alpinelinux.org/): a small muslc based distribution focused on embedded systems and servers. It has stable releases and a rolling model.

* [Devuan Linux](https://devuan.org/): Debian without systemd, and it has extended support. A more user friendly solution, geared towards the desktop, would be [MX Linux](https://mxlinux.org/).

* [OpenSUSE Linux](https://www.opensuse.org/): usually forgotten, however, one of the best distributions out there. [GeckoLinux](https://geckolinux.github.io/): is a more user friendly solution based on OpenSUSE.

* [CentOS Linux](https://www.centos.org/): the community version of RHEL. It is the most stable distribution out there, also the one that ages the most. It is widely used at CERN and FERMI. With CentOS 8 release, there is a new way to get officially supported software faster, see CentOS Streams.

* [OpenIndiana Illumos](https://www.openindiana.org/): based on Illumos, the descendant of OpenSolaris; it targets workstations and servers, and it is kept somewhat up to date. There is also [OMNI OS](https://omniosce.org/), which is better suited for servers.

* [NetBSD](http://netbsd.org/): targets embedded systems, yet it is a joy to use it, simple and _hacky._

* [FreeBSD](https://www.freebsd.org/) and [DragonflyBSD](https://www.dragonflybsd.org/).

---

### More dynamic distributions and OSs, mostly targeting desktops

* [Void Linux](https://voidlinux.org/): a DIY distribution: offers glibc and muslc libraries, systemd-free, yet powerful and follows a rolling release model, supports various archs.

* See [OpenSUSE Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed). See [Devuan](https://devuan.org/) with Ceres repositories.

* [Artix Linux](https://artixlinux.org/): Arch-based OpenRC/Runit distribution.

* [KDE Neon Linux](https://neon.kde.org/download): Ubuntu-based KDE focused distribution. It is officially developed by the KDE team.

* [Fedora Linux](https://getfedora.org/): RedHat backed distro which focuses on more up-to-date software.

* [GuixSD](https://www.gnu.org/software/guix/): a fully libre distribution centered arround the Guix package/system manager.

## Terminal applications

No "low level" utilities will be listed below, just the programs that you will find yourself dealing directly, this means no mention to tar, grep, awk, sed, cups, gvfs, etc. However, they are all wonderful programs.

### Shell

* [Mksh](https://www.mirbsd.org/mksh.htm): it is one of the fastest, smallest yet featureful shells available. It runs pretty much anywhere. It is the default shell in Android.

### Helpers

* [Abduco](https://github.com/martanne/abduco) and [dvtm](https://github.com/martanne/dvtm): created by the same person, [Marc Andrè Tanner](https://github.com/martanne). Abduco provides session management within the terminal. Dvtm is a terminal multiplexer. Combined, they provide the same functionality as [GNU Screen](https://www.gnu.org/software/screen/) or [Tmux](https://github.com/tmux/tmux), GNU Screen or Tmux are also very nice multiplexers, and you are encouraged to try them.

### System tools

* [Neofetch](https://github.com/dylanaraps/neofetch): prints system information directly to the terminal with a nice logo. Use [Inxi](https://github.com/smxi/inxi) if you would like a richer output.

* [Lm_sensors](https://github.com/groeck/lm-sensors): monitor temperatures, control fans, etc.

* [Bluez](http://www.bluez.org/): bluetooth management. If a graphical user interface is being used, then [Blueman](https://github.com/blueman-project/blueman) will be of great help.

* [Htop](http://hisham.hm/htop/): a wonderful task manager, use it.

* [Udisks](https://github.com/storaged-project/udisks): mount and unmount drives or volumes with no difficulties.

* [Vifm](https://vifm.info/): vi-like file manager, simple yet complete with some nifty features. [Ranger](https://ranger.github.io/): complete file manager in the terminal, even with fancy columns, etc; and it is fully customizable! Another file manager would be [Midnight Commander (mc)](https://midnight-commander.org/). If a much lighter alternative is wanted [nnn](https://github.com/jarun/nnn#file-handling) is also wonderful. There is [ncdu](https://dev.yorhel.nl/ncdu) too, which is a disk usage analizer.

* [Rsync](https://rsync.samba.org/): an outstanding file transfer utility. It is mainly targeted towards incremental transfers. It is mainly used for backup or complex copying.

* [Borg](https://github.com/borgbackup/borg): as it says in it's description: Deduplicating archiver with compression and authenticated encryption. It works wonders for backups. A similar tool would be [Restic](https://restic.net/).

* [Atool](http://www.nongnu.org/atool/): a multi-format archiver and extractor.

#### Power management

* [TLP](https://linrunner.de/en/tlp/tlp.html): The Linux Power manager. If you have a laptop, make sure to install it and configure it properly if needed.

* [Powertop](https://01.org/powertop/): power monitoring with togglable options to further tweak your power consumption.

### Network

* [Curl](https://curl.haxx.se/): the Swiss knife tool to transfer data with URLs. A less flexible, yet simpler and equally useful is [wget](https://www.gnu.org/software/wget/).

* [Rtorrent](https://github.com/rakshasa/rtorrent): powerful torrent management utility. I recommend using [Pyroscope's extended distribution](https://github.com/pyroscope/rtorrent-ps). If a GUI is needed then [Qbittorrent](https://www.qbittorrent.org/) or [Transmission](https://transmissionbt.com/) are available with optional terminal backends.

* [WeeChat](https://weechat.org/): extensible and powerful IRC client. There are extensions to expand its compatibility with other protocols.

* [Nmap](https://nmap.org/): the Swiss knife tool to analyze networks.

* [Wireshark](https://www.wireshark.org/): network package analysis tool. Qt backend recommended.

* [Icecast](http://icecast.org/): is free server software for streaming multimedia.

* Extras: _[vsftpd](https://security.appspot.com/vsftpd.html), [lftp](http://lftp.tech/), [Nextcloud](https://nextcloud.com/)._

### Misc

* [Asciinema](https://asciinema.org/): terminal recorder.

* [Clamav](https://www.clamav.net/): anti-virus.

* [Toilet & Libcaca](http://caca.zoy.org/): colourful large text in the terminal and ascii art.

* [Newsbeuter](https://newsbeuter.org/): Atom and RSS feeds in your terminal.

## Text editors

* [Vis](https://github.com/martanne/vis): a vi-like editor based on Plan 9's structural regular expressions. Fuses the best of Vi(m) and Sam editors. Minimal and extensible by nature using lua.

* [GNU Emacs](https://www.gnu.org/software/emacs/): definitely the most powerful editor out there. Extensible as you wish, and even more powerful, though the learning curve is horrible. It has some of the most mesmerizing addons to have ever existed such as [org-mode](http://orgmode.org/), [magit](https://magit.vc/), [evil](https://github.com/emacs-evil/evil) or [org-brain](https://github.com/Kungsgeten/org-brain).

* [Joe](https://joe-editor.sourceforge.io/): it is a minimal, yet severely overlooked editor that resembles the way editors used to be. It is more feature packed than what it seems, and it supports emacs, wordstar and nano emulation.

* [Microsoft Visual Studio Code](https://code.visualstudio.com/): a modern text editor with everything you may need. While not as small as the rest, it is beautiful, fast, and the best for embedded development with the combination of [PlatformIO](https://platformio.org/). Note that the binaries distibuted directly from the web page are not under a libre licence.

## Programming

* [Git](https://git-scm.com/): most widely used version control system. [Tig](https://jonas.github.io/tig/): terminal interface for git. TODO: fossil.

* [Gdb](https://www.gnu.org/software/gdb/) with [Cgdb](https://cgdb.github.io/): the most flexible debugger to have ever existed. Supports a plethora of languages.

* [Radare2](https://www.radare.org/r/index.html): wonderful TUI disassembler. [Cutter](https://github.com/radareorg/cutter) is a GUI for it.

* [Valgrind](http://valgrind.org/): a wonderful runtime analysis tool, specially for memory inspection.

* [Cppcheck](http://cppcheck.sourceforge.net/): static analysis tool for C/C++ code. MISRA standard is mostly complete.

* [Meson](https://mesonbuild.com/): complete, easy and modern build system. [Autotools](https://www.gnu.org/software/automake/manual/html_node/Autotools-Introduction.html): for simpler projects and compatibility, read [this guide/book](https://autotools.io/index.html) as a great introduction.

* [Docker](https://www.docker.com/): container technology (OS-level virtualization), only available for Linux.

* [QtCreator](https://wiki.qt.io/Qt_Creator): one of the most powerful IDEs out there. It aims for C/C++, QML/Javascript and Python support. Embeds Qt and Qt Quick very nicely, but its use is secondary.

* [Kdevelop](https://www.kdevelop.org/): a more traditional IDE than QtCreator, smaller, yet it targets the same languages as QtCreator + PHP. It does not, however, offer as much as QtCreator does.

* [Monodevelop](http://www.monodevelop.com/): IDE for C#, F#, and .NET.

* [ZeroBrane](https://studio.zerobrane.com/): everything Lua IDE.

* [Leksah](http://leksah.org/): Haskell IDE.

* [Ht](http://hte.sourceforge.net/): hex editor in your terminal. It has support for disassembly.

### Embedded systems

* [SimAVR](https://github.com/buserror/simavr): simulates AVRs. With the help of GDB it may be used as an advance debugger.

* TODO

## Browsers - Web

* [Firefox](https://www.mozilla.org/en-US/firefox/new/): Firefox web browser.

* [Iridium](https://iridiumbrowser.de/): de-googled Chromium.

* [Falkon](https://www.falkon.org/): QtWebEngine based browser; another WebEngine-based browser, targeted towards heavy keyboard use (vi keybindings) is [Qute Browser](https://qutebrowser.org/). [Otter Browser](https://otter-browser.org/) is also worth checking out.

* [W3m](http://w3m.sourceforge.net/): terminal web browser with support for images.

* [Links](http://links.twibright.com/): lightweight terminal web browser.

* [HTTrack](http://www.httrack.com/): page cloning utility. It has an official GUI HTTraQt.

### Recommended Add-ons for Firefox (most are Chromium compatible)

* [uMatrix](https://github.com/gorhill/uMatrix): content filtering (javascript, media, CSS, etc).

* [uBlock Origin](https://github.com/gorhill/uBlock): ad and tracker blocker.

* [Decentraleyes](https://decentraleyes.org/): local CDN to serve the most commonly requested packages.

* [Cookie AutoDelete](https://github.com/Cookie-AutoDelete/Cookie-AutoDelete): easy-peasy cookie management.

* [Violentmonkey](https://violentmonkey.github.io/): userscript manager. There is also [Greasemonkey](https://www.greasespot.net/).

## Multimedia

### Players

* [Audacious](https://audacious-media-player.org/): wonderful audio player. Supports pretty much everything someone could dream of, plus it offers a Winamp interface.

* [Cmus](https://cmus.github.io/): terminal audio player, small, fast and powerful. As an alternative there is also [Moc](http://moc.daper.net/).

* [Feh](https://feh.finalrewind.org/): fast and light image viewer for X11. Another one would be [sxiv](https://github.com/muennich/sxiv).

* [Gwenview](https://www.kde.org/applications/graphics/gwenview/): everything you would be expecting from an image viewer.

* [Mpv](https://mpv.io/): sleek video player. Minimal, customizable to the extreme. An easier alternative, yet just as great is [Vlc](https://www.videolan.org/vlc/index.html).

* [Cheese](https://wiki.gnome.org/Apps/Cheese): webcam application.

### Media Creation

#### Audio

* [Audacity](https://www.audacityteam.org/): small, yet powerful audio editing software. Works wonders when combined in a video-editing pipeline.

* [Fre:ac](https://www.freac.org/): audio transcoder.

* [Ardour](https://www.ardour.org/): complete DAW.

* [LMMS](https://lmms.io/): music production (music synthesither).

* [MuseScore](https://musescore.org/en): professional music notation, while simple and fully flexible. [Denemo](http://www.denemo.org/): another great music notation program, based on the great [LilyPond](http://lilypond.org/). [Rosegarden](https://www.rosegardenmusic.com/): a quite complete solution to music production, from notation to synthesis to MIDI playback.
  
* [Sonic Visualiser](https://sonicvisualiser.org/): audio viewer and analyzer.

* [Radium](http://users.notam02.no/%7Ekjetism/radium/index.php): amazing music editor with a unique feel.

* [MuSe](http://www.muse-sequencer.org/index.html): complete MIDI/Audio sequencer.

* [Zynaddsubfx](http://zynaddsubfx.sourceforge.net/): really nice audio synthesizer, the most complete out there.

* [Milkytracker](http://milkytracker.titandemo.org/), [Schismtracker](http://schismtracker.org/), [Klystrack](https://kometbomb.github.io/klystrack/) and [Protracker & Fasttracker II clone](https://16-bits.org/index.php): precious pieces of computing history, the beloved trackers.

* [Bristol](http://bristol.sourceforge.net/): (ancient) synthesiser emulator, supports several models.

* [GNU Radio](https://www.gnuradio.org/): software defined radio. [Gqrx SDR](http://gqrx.dk/): receiver based on GNU Radio.

#### Graphics (2D)

* [Krita](https://krita.org/): digital painting program; alternative to Adobe Illustrator.

* [Gimp](https://www.gimp.org/): GNU Image Manipulation Program; great alternative to Adobe Photoshop.

* [Grafx2](http://pulkomandy.tk/projects/GrafX2): an Amiga-era pixel art painting program.

* [Azpainter](http://azsky2.html.xdomain.jp/): beautiful lightweight 16bit drawing application; ([in english](https://osdn.net/projects/azpainter/)).

* [Inkscape](https://inkscape.org/en/): vector painting software.

* [Darktable](https://www.darktable.org/): photography workflow application and raw developer.

* [FontForge](https://fontforge.github.io/en-US/): create or edit fonts.

#### Video - Animation

* [Obs](https://obsproject.com/): record video sources and broadcast them.

* [Blender](https://www.blender.org/): a complete and professional 3D creation suite.

##### Render Engines

* [LuxCore](https://luxcorerender.org/): unbiased (physically accurate) render, supports OpenCL.

* [Appleseed](https://appleseedhq.net/): physically-based render.

* [YafaRay](https://www.yafaray.org/): physically-based render widely used for architectural visualization.

---

* [OpenToonz](https://opentoonz.github.io/e/): 2D painting and animation suite.

* [Natron](https://natrongithub.github.io/): compositor for visual effects and the graphics industry. Great for post-production.

* [Kdenlive](https://kdenlive.org/en/): pretty much the best open source video editing software, with professional quality. TODO: shotcut.

* [Aegisub](http://www.aegisub.org/): for subtitle editing. There is also [Gaupol](https://otsaloma.io/gaupol/) if you prefer.

* [Handbrake](https://handbrake.fr/): video transcoder. For .mkv there is a better tool [MKVToolsNix](https://mkvtoolnix.download/).

## Document creation

For office utilities, please, refer to the next section. Use [Hunspell](https://hunspell.github.io/) or [Aspell](http://aspell.net/) for spelling.

* [LaTeX](https://www.latex-project.org/): typesetting software, mainly aimed at high quality publications, though it suites everyone needs. A wonderful editor for LaTex is [TeXStudio](https://www.texstudio.org/).

* [Scribus](https://www.scribus.net/): a publishing application. Works wonders for flyers and magazines as well as presentations. Supports LaTeX.

* **Markdown**: [Ghostwriter](https://github.com/wereturtle/ghostwriter): a Qt editor with Pandoc import-export support. [Marker](https://github.com/fabiocolacio/Marker): a Gtk editor with Pandoc import-export support.

### Document viewers

* [Okular](https://www.kde.org/applications/graphics/okular/): it is sleek, complete and supports pretty much any format imaginable.

* [Zathura](https://pwmt.org/projects/zathura/): simple, keyboard driven but complete viewer.

## Office Software

### Suites

* [Libreoffice](https://www.libreoffice.org/): a complete alternative to Microsoft Office, pretty much fully compatible.

* [Onlyoffice](https://www.onlyoffice.com/): a simple yet complete office suite, compatible with Microsoft Office.

### Word

* [Abiword](https://www.abisource.com/): a small and simple word processing program, has nothing fancy in it.

* [Wordgrinder](http://cowlark.com/wordgrinder/): a terminal (curses) program to edit and export documents, supports .docx.

### Excel

* [Gnumeric](http://www.gnumeric.org/): rich spreadsheet software.

* [Sc-im](https://github.com/andmarti1424/sc-im): terminal based spreadsheet program.

* [GNU PSPP](https://www.gnu.org/software/pspp/): it is more an alternative to SPSS than to Excel, however, it works wonders too.

### Email

* [Thunderbird](https://www.thunderbird.net/): complete email client with full GPG support.

* [Kmail](https://www.kde.org/applications/internet/kmail/): simple, lightweight but feature-rich client.

* [Sylpheed](http://sylpheed.sraoss.jp/en/): very lightweight and simple e-mail client.

* [Mutt](http://www.mutt.org/): TUI email client.

### Money Management

* [Money Manager EX](https://www.moneymanagerex.org/): modern, simple and complete cash manager.

* [GNU Cash](https://www.gnucash.org/): a very well-know open source software, unmatched with its flexibility.

### Scheduling

* [Calcurse](https://www.calcurse.org/): terminal based scheduler.

* See GNU Emacs packages (calendar and org).

### Diagraming

* [Draw.io](https://www.draw.io/): wonderful diagraming tool. From basic drawings, to flowcharts and organization. A more complex but also more powerful system is [Graphviz](https://graphviz.org/), specially with the _dot_ language.

## Science - Engineering

### General

* [Jupyter](https://jupyter.org/): notebook. [Available kernels](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels). Also worth checking out [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/).

* [Octave](https://www.gnu.org/software/octave/): Matlab compatible scientific programming language. Extra functionality can be found at [Octave Forge](https://octave.sourceforge.io/).

* [Scilab](http://www.scilab.org/): complete alternative to Matlab or Octare thereof.

* [OpenModelica](https://www.openmodelica.org/): a complete Modelica solution. Models physical systems and controllers.

* **Plotting**: [GNU Plot](http://gnuplot.info/): advance and flexible plotting tool. [PLplot](http://plplot.org/). [MathGL](http://mathgl.sourceforge.net/doc_en/Main.html). TODO, pgfplots and pyplot

### Mathematics

* [COIN-OR](https://www.coin-or.org/): complete suite for optimization and general operational research. CMPL is their own mathematical programming language. Coliop is a basic GUI to write CMPL.

* [SageMath](https://www.sagemath.org/): complete mathematical suite.

* [Maxima (WxMaxima)](http://maxima.sourceforge.net/): algebra software.

* [Gap](http://www.gap-system.org/):  computational discrete algebra, with emphasis on computational group theory.

* [Xcas](http://www-fourier.ujf-grenoble.fr/~parisse/giac.html): computer algebra system.

* [Cadabra](https://cadabra.science/): symbolic computer algebra system (CAS).

* [Singular](http://www.singular.uni-kl.de/): CAS for polynomial computations.

* [OpenTURNS](http://www.openturns.org/): uncertainty treatment and measurement.

### Design - Mechanical - Simulation

* [Gmsh](http://gmsh.info/): designer, mesh generator and post-processor.

* [LibreCAD](https://librecad.org/): 2D CAD drawing solution.

* [FreeCAD](https://www.freecadweb.org/): complete 3D design solution and provides FEM and CFD modules.

* [Solvespace](http://solvespace.com/index.pl): parametric 2D/3D CAD.

* [OpenSCAD](http://www.openscad.org/): parametric design (Python based).

* [BRL-CAD](http://brlcad.org/): the oldest CAD available still in development.

* [gCAD3D](http://www.gcad3d.org/): wonderful 2D/3D CAD program, lacks plan design.

* [HeeksCAD](https://github.com/Heeks/heekscnc): CNC tooling. There is also [PyCAM](http://pycam.sourceforge.net/).

* [Cura](https://github.com/Ultimaker/Cura): 3D printing suite.

* [LinuxCNC](http://linuxcnc.org/): CNC controller. [CAMotics](https://github.com/CauldronDevelopmentLLC/CAMotics) is for 3-axis CNC GCode simulation.

* [Netgen/NGSolve](https://ngsolve.org/): complete mesher.

* [Meshlab](http://www.meshlab.net/): advance remesher.

The Salome Platform

* [Salome Meca](http://www.salome-platform.org/): complete engineering platform, from design, to meshing, to problem description and boundary conditions, to simulation and visualization. It is composed of smaller pieces of software which are described below.

* [Code Aster](https://www.code-aster.org/): a mechanical and thermal solver.

* [Code Saturne](https://www.code-saturne.org/cms/): CFD solver.

---

* [OpenFoam](https://openfoam.org/): THE open source CFD.

* [ElmerFEM](https://www.csc.fi/web/elmer): fluid dynamics, structural mechanics, electromagnetics, heat transfer and acoustics FEM.

* [Calculix](http://www.calculix.de/): FEM for dynamic, static structures and thermal solutions.

* [GetDP](http://getdp.info/): general environment for the treatment of discrete problems.

* Check license. [AMITEX_FFTP](http://www.maisondelasimulation.fr/projects/amitex/html/index.html): solver based on FFTs for non-linear mechanical analysis on heterogeneous unit-cells.

* [Agros 2D](http://www.agros2d.org/): simulator of physical problems based on the Hermes library.

* [MFront/TFEL](http://tfel.sourceforge.net/): code generation tool dedicated to material knowledge and its design. Has interfaces to some most libre software listed here.

* [LAMMPS](https://lammps.sandia.gov/): mulecular dynamics simulator.

* [Open TELEMAC-MASCARET](http://opentelemac.org/): integrated suite of solvers for use in free-surface flows.

* [Polyphemus](http://cerea.enpc.fr/polyphemus/): air dispersion and pollution.

* [AERMOD](https://www.epa.gov/scram/air-quality-dispersion-modeling-preferred-and-recommended-models#caline): air dispersion and pollution simulator.

* [Dakota](https://dakota.sandia.gov/): advance optimizer.

* [Paraview](https://www.paraview.org/): THE data visualization program, it is a wonderful piece of software.

* [Vislt](https://wci.llnl.gov/simulation/computer-codes/visit/): visualization software.

* [3DSlicer](https://www.slicer.org/): 3D visualization software specialized in volumetrics.

* **Not Open Source** [Simscale](https://www.simscale.com/): online web application, complete simulation solution which only uses libre software (mentioned above). Completely free for students.

---

* [ITOM](https://itom.bitbucket.io/): suite for operating measurement systems.

### Electronics

* [KiCAD](http://kicad-pcb.org/): PCB design and simulation.

* [gEDA](http://www.geda-project.org/): complete EDA suite.

* [XCircuit](http://opencircuitdesign.com/xcircuit/): circuite schematic design.

* [Magic VLSI](http://opencircuitdesign.com/magic/): VLSI layout tool.

* [IRSIM](http://opencircuitdesign.com/irsim/): switch-level simulator.

* [Qucs](http://qucs.sourceforge.net/): as its name expresses _Quite Universal Circuit Simulator._

* [KTechLab](https://github.com/ktechlab/ktechlab): IDE for microcontrollers and electronics, as well as a simulator.

* [GTKWave](http://gtkwave.sourceforge.net/): wave viewer.

* [FlatCAM](http://flatcam.org/): PCB milling.

### Others

* [SUMO](https://www.dlr.de/ts/en/desktopdefault.aspx/tabid-9883/16931_read-41000/): Simulation of Urban MObility, simulates vehicles, pedestrians and public transport mobility.

### Networking

* [GNS3](https://gns3.com/): network simulator/analyzer.

## Games

### Rogue like

* [Angband](http://rephial.org/): a terminal roge-like game based on Tolkien's work.

* [Nethack](http://www.nethack.org/): one of the oldest rogelikes still in development, play in the terminal.

* [Cdda](http://en.cataclysmdda.com/): Cataclysm Dark Days Ahead, a terminal roge-like whose setting is in a modern apocalypse.

* [Crawl](https://crawl.develz.org/): may be played in the terminal, another great roge-like.

* [CotD](https://github.com/gwathlobal/CotD): City of the Dammed. A terminal roge-like of a battle of Angels and Demons in the streets of a Human city.

* [ToME4](https://te4.org/): a roge-like based on Tolkien's work.

* [Keeprrl](https://keeperrl.com/): dungeon builder with a roge-like touch.

### Shooters

* [Urban Terror](https://www.urbanterror.info/home/): an old school shooter (yet fun and enjoyable as ever).

* [Xonotic](http://xonotic.org/): a Quake-like game, get ready to get killed and have fun.

* [AssaultCube](https://assault.cubers.net/): old school and very lightweight shooter.

* [Taisei](https://taisei-project.org/): fangame recreating the queen of bullet hell games, Tohou.

### Adventure

* [Minetest](https://www.minetest.net/): a Minecraft clone that is just as good.

### RPGs

* [Flare](http://flarerpg.org/): an old school RPG like Diablo.

* [ManaPlus](http://manaplus.org/start): a client for the MMO _The Mana World._

### RTS/Strategy

* [0ad](https://play0ad.com/): an Imperium, Age of Empires clone.

* [Wesnoth](https://wesnoth.org/): a fantasy turn-based strategy game, great fun.

* [Freeciv](http://freeciv.org/): game inspired by the history of human civilization.

* [MegaGlest](https://megaglest.org/): an old looking 3D fantasy strategy game.

* [Warzone 2100](http://wz2100.net/): an old school RTS.

### Simulation

* [FlighGear](http://home.flightgear.org/): professional flight simulator.

* [OpenTTD](https://www.openttd.org/en/): game based on Transport Tycoon Deluxe.

* [Simutrans](https://www.simutrans.com/en/): transport simulation.

### Miscelanea

* [GNU Chess](https://www.gnu.org/software/chess/): play chess.

### Emulators

* [Dolphin](https://es.dolphin-emu.org/): Game Cube and Wii emulator.

* [Mednafen](https://mednafen.github.io/): NES, SNES, GB(C), GBA, PSX, Saturn, Genesis, ... emulator. There is [Mednaffe](https://github.com/AmatCoder/mednaffe), a GUI for it.

* [Mgba](https://mgba.io/): a fresh GBA emulator.

* [Mupen64Plus](http://mupen64plus.org/): N64 emulator. Use [M64Py](http://m64py.sourceforge.net/) as GUI.

* [PCSX2](https://pcsx2.net/): Play Station 2 emulator.

* [Desmume](https://github.com/TASVideos/desmume/): NDS emulator.

* [Citra](https://citra-emu.org/): 3DS emulator.

* [DosBox](https://www.dosbox.com/): DOS emulator.

* [Fuse](http://fuse-emulator.sourceforge.net/): Spectrum emulator.

* [Yaze](http://www.mathematik.uni-ulm.de/users/ag/yaze-ag/): Z80 emulator.

* [Simh](http://simh.trailing-edge.com/): emulates historical masterpieces.

### Engines

* [Solarus](http://www.solarus-games.org/): a 2D RPG game editor like RPG Maker written in Python.

* [Löve](https://love2d.org/): a 2.5D Lua framework.

* [Godot](https://godotengine.org/): a complete game engine with C# and C++ support.

* [Torque 2D & 3D](http://www.garagegames.com/): not the most modern game engine, though it is more than enough for most projects.

* [Irrlicht](http://irrlicht.sourceforge.net/): great engine library.

* [Tiled](https://www.mapeditor.org/): utility to easily create 2D maps.

## Miscellaneous

* [KeePassXC](https://keepassxc.org/): password storage, compatible with KeePassX.

* [Syncthing](https://syncthing.net/): synchronization by yourself for yourself. I has clients for all mayor platforms.

* [Remmina](http://www.remmina.org/wp/): remote desktop.

* [GParted](https://gparted.sourceforge.io/): graphical utility to manage partitions. There is also [KDE Partition Manager](https://www.kde.org/applications/system/kdepartitionmanager/).

* [K3B](https://www.kde.org/applications/multimedia/k3b/): CD/DVD/BD burning, ripping utility. Install the necessary programs to expand it's usability.

* [Iat](https://sourceforge.net/projects/iat.berlios/): converts from an to ISO9660, CUE, BIN, etc.

* [Cdrtools](http://cdrtools.sourceforge.net/private/cdrecord.html): a CD/DVD/BluRay helper.

## Extras

Here goes a little extra section regarding some of the technologies that I quite like but are not suitable for the previous section.

### Programming languages

* **C** [GCC](https://gcc.gnu.org/) or [Clang](https://clang.llvm.org/): the low level language. The grandfather of the modern world. A wonder in itself, by it's simplicity and flexibility. If an in-depth analysis of the code is required, there is [Frama-C](https://frama-c.com). A C compiler targeted to more retro/microcontroller CPUs is [Small Device C Compiler](http://sdcc.sourceforge.net/).

* **Modern C++** [GCC](https://gcc.gnu.org/) or [Clang](https://clang.llvm.org/): please, use the modern features the language gives you! Low level language, though several times more complete (*and dificult* when it comes to learning it) than C.

* **Fortran** [GNU Fortran](https://gcc.gnu.org/fortran/): though it may seem outdated, it is still widely used in HPC and older software for its unmatched speed.

* [Ada/Spark](https://www.adacore.com/community): high-performance security critical programming language. It is not widely used in the *libre* software world, but it definitely has owned its place in the industry.

* [Rust](https://www.rust-lang.org/en-US/): a higher level language that C/C++ yet it targets low level systems. It's main focus is on memory security.

* [Julia](https://julialang.org/): a language targeted towards high performant code, specially analisys and science.

* **Lisp/Scheme** [Sbcl](http://www.sbcl.org/), [GNU Guile](https://www.gnu.org/software/guile/) or [Racket](https://racket-lang.org/): just learn it.

* [Lua](https://www.lua.org/) and [LuaJIT](http://luajit.org/): a wonderful little language geared specially towards embedding.

* [Elixir](https://elixir-lang.org/): functional language built on top of the ErlangVM (BEAM). It is mostly targeted to fault tolerance systems and web services with scalability in mind. Much recommended. [Credo](https://github.com/rrrene/credo) is a static analyzer for it.

* [Haskell](https://www.haskell.org/): _the_ functional language.

* [R](https://www.r-project.org/): a language mainly aimed at statistics. [Rkward](https://rkward.kde.org/Main_Page) is a small and lightweight, IDE for it. [Rstudio](https://www.rstudio.com/): is the most complete and well-known IDE for R.

* [F#](https://fsharp.org/): functional meets .NET.

* [UML Umbrello](https://umbrello.kde.org/): UML diagramming/modeller.

* **Formal languages** [F*](https://www.fstar-lang.org/) and [Coq](https://coq.inria.fr/).

* **Go** [Gcc-go](https://gcc.gnu.org/onlinedocs/gccgo/) or [Go](https://golang.org/): developed by Google, for the web, great for backends or anything related to web.

* **Prolog** [Gprolog](http://gprolog.org/) or [SWI Prolog](http://www.swi-prolog.org/): the greatest logical language out there.

* [SuperCollider](https://supercollider.github.io/): a platform for audio synthesis and algorithmic composition.

* **Hardware description languages:** [GHDL](http://ghdl.free.fr/): VHDL compiler. [Iverilog](http://iverilog.icarus.com/): Verilog compiler.

* **Others worth looking at:** [Coq](https://coq.inria.fr/): language for formal verification. [Python](https://www.python.org/) quick scriptable and widely used language (specially in science), [Nuitka](https://nuitka.net/) is a compiler for it.

* **General tools:** [Crucible](https://github.com/GaloisInc/crucible): library for symbolic simulation of imperative programs. [SAW-Script](https://github.com/GaloisInc/saw-script): scripting language for SAW (Software Analysis Workbench).

#### Web

As a recommendation, use javascript only where necesary and sparsely.

* [TypeScript](http://www.typescriptlang.org/): make yourself a favour and use it instead of JavaScript. There is also [PureScript](http://www.purescript.org/) if you prefer the Haskell way.

* **Transpilers to JavaScript:** [Rust Yew](https://github.com/DenisKolodin/yew), the goodness of Rust in all of its glory (targets WASM). [Elm](https://elm-lang.org/): modern language to create reliable webapps (front-end). [Go GopherJS](https://github.com/gopherjs/gopherjs): compiler form Go to JavaScript.

* [Phoenix](https://phoenixframework.org/): there are quite a few frameworks out there, but Phoenix, written in Elixir, is definitely the best one out there; complete and flexible. Another framework that I personally like too is [Lapis](http://leafo.net/lapis/), for Lua and Moonscript.

* [Terraform](https://www.terraform.io/): infraestructure management system.

* [Saltstack](https://www.saltstack.com/): automation and configuration of any system.

* [Kubernetes](https://kubernetes.io/): system for automating deployment, scaling, and management of containerized applications.

* **Static Builders:** [Zola](https://www.getzola.org/): same, but with Rust, preferred by author. [Hugo](https://gohugo.io/): great(est) static pages generator, Go based. [Hakyll](https://jaspervdj.be/hakyll/): an alternative based on Haskell.

* **Extra bits, none Open Source** [DNSimple](https://dnsimple.com/): as its name implies, simple, yet complete domain acquisition service with Let's Encrypt certificates; and they fully support open source. [Digital Ocean](https://www.digitalocean.com/): complete hosting solution, not the cheapest, but one of the easiest and complete ones. [UpCloud](https://www.upcloud.com/): another nice hosting solution.

### Databases

* [Sqlite](https://www.sqlite.org/index.html): a lightweight SQL solution.

* [PostgreSQL](https://www.postgresql.org/): extremely powerful, and a tad complex ORDBMS.

* [MariaDB](https://mariadb.org/): MySQL compatible (forked) solution widely used in the industry.

* [Redis](https://redis.io/): in-memory storage, there are interfaces for every language imaginable.

### Social Media

* [LibrePay](https://liberapay.com/): similar to Patreon. One can donate to individuals, projects, companies or be given money for ones work.

* [Mastodon](https://joinmastodon.org/): twitter like network, but decentralized and several times better (btw, you don't _tweet,_ you **toot**). Mastodon is based on [GNU Social](https://gnu.io/social/), which is also great, and it is compatible with it. Another alternative compatible with the OStatus systems (*Gnu Social and Mastodon*) is [Pleroma](https://pleroma.social), which is written in Elixir.

* [PeerTube](https://joinpeertube.org/en/): decentralized video hosting network.

* [Matrix](https://matrix.org/blog/home/): _An open network for secure, decentralized communication._ [Diaspora*](https://diasporafoundation.org/) is another wonderful social network following the same principle.

* [Wire](https://wire.com/en/): a _collaboration_ network, similar to Slack or Telegram, but much better. There is also [Mattermost](https://www.mattermost.org/), which is a lot more _enterprisy,_ so up to you.

* [Mumble](https://wiki.mumble.info/wiki/Main_Page): VoIP.

* [GNU FM (Libre FM)](https://gnu.io/fm/): relative of GNU Social, but directed for music streaming.

### Project management

* **Git**: [Gitea](https://gitea.io/en-US/): self-hosted Git. Similar to Github; and much lighter than [GitLab](https://about.gitlab.com/), which is a more complete solution, and it is used by major companies and projects. If the solution has to be simple and responsive, there is [Cgit](https://git.zx2c4.com/cgit/) plus [Gitolite](http://gitolite.com/gitolite/).

* **Project management:** [Odoo](https://www.odoo.com/): complete ERP and CRM solution, the open-source version does not have the most advance (and usually handy) tools. [ERPNext](https://erpnext.com/): complete ERP solution. [SuiteCRM](https://suitecrm.com/): complete CRM solution.

* **Project management (code-based):** [Tuleap](https://www.tuleap.org/), complete software solution for any project. [Phabricator](https://phacility.com/) is a _down to the code_ alternative.
