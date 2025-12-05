---
layout: page
title: Kojo Download
permalink: /kojo-download
kojo_version: 2.9.32
---

[Kojo](/kojo) is [open source software](https://github.com/litan/kojo), and is freely available. You can download and install Kojo based on the instructions and installers provided on this page.

---

{% capture base %}https://github.com/litan/kojo/releases/download/{{ page.kojo_version }}_release{% endcapture %}
{% capture version_uscore %}{{ page.kojo_version | replace: ".", "_" }}{% endcapture %}

{% capture unixFileWithJre %}Kojo_unix_{{ version_uscore }}_with_jre.sh{% endcapture %}
{% capture unixInstallerWithJre %}{{ base }}/{{ unixFileWithJre }}{% endcapture %}
{% capture unixFileWithoutJre %}Kojo_unix_{{ version_uscore }}.sh{% endcapture %}
{% capture unixInstallerWithoutJre %}{{ base }}/{{ unixFileWithoutJre }}{% endcapture %}

{% capture winInstaller %}{{ base }}/Kojo_windows-x64_{{ version_uscore }}_with_jre.exe{% endcapture %}
{% capture macInstaller %}{{ base }}/Kojo_macos_{{ version_uscore }}_with_jre.dmg{% endcapture %}
{% capture zipDistribution %}{{ base }}/Kojo_{{ version_uscore }}.zip{% endcapture %}

#### Quick Links

Click on a button below to download Kojo for your platform/OS:

<div class="row ml-1 mb-4">
  <a href="{{ unixInstallerWithJre }}">
    <button type="button" class="btn btn-primary btn-theme-bg">Linux</button>
  </a>

  <a href="{{ winInstaller }}">
    <button type="button" class="btn btn-primary btn-theme-bg">Windows</button>
  </a>

  <a href="{{ macInstaller }}">
    <button type="button" class="btn btn-primary btn-theme-bg">Mac</button>
  </a>

  <a href="{{ unixInstallerWithoutJre }}">
    <button type="button" class="btn btn-primary btn-theme-bg">R-Pi</button>
  </a>

  <a href="{{ zipDistribution }}">
    <button type="button" class="btn btn-primary btn-theme-bg">X-Platform</button>
  </a>
</div>

---

#### Links with detailed instructions

Click on a link below to be taken to the corresponding download section:
<div>
  Kojo downloads:
      <a href="#unix">Linux/Unix</a> | <a href="#win">Windows</a> | <a href="#mac">Mac</a> | <a href="#rpi">Raspberry Pi</a> | <a href="#chromebook">Chromebook</a> | <a href="#crossplatform">Cross Platform</a>
      <br/>
  Download related links:
      <a href="https://docs.kogics.net/faq/installation-faq.html">Installation FAQ</a> | <a href="#media">Media Files</a> | <a href="#install4j">Installer technology</a>
      <br/><br/>
</div>

New Kojo Releases are announced on the [Kojo Blog](/blog). You can subscribe to the blog feed to be notified.

---

<h5 id="unix">Linux/Unix</h5>

Inside a terminal, run `uname -m` or `arch` to determine whether you are on a 64 bit or a 32 bit (x86 architecture) system.
* If the output is `x86_64`, you are on a 64 bit system.
* If the output is `i686`, `i586`, `i486`, or `i386`, you are on a 32 bit system.
Based on the above output, choose the appropriate installer:

**64 bit Linux/Unix**

[Kojo Installer (shell script)]({{ unixInstallerWithJre }}) (Version: {{page.kojo_version}})

*Instructions:*
* Download the Kojo installer (shell script). Then run it by opening up a Terminal Window, going to the directory where the installer is located, and running: `sh {{unixFileWithJre}}`.
* After Kojo is installed, you can run it from the Desktop (if you opted for a Desktop shortcut), from the Development application category/group, or from the bin directory inside your Kojo install.
* The Kojo shortcut is named Kojo Learning Environment.


**32-bit Linux/Unix**

[Kojo Installer (shell script)]({{ unixInstallerWithoutJre }}) (Version: {{page.kojo_version}}, needs Java 8, 11, or 17)

*Instructions:*
* Download the Kojo installer (shell script). Then run it by opening up a Terminal Window, going to the directory where the installer is located, and running: `sh {{unixFileWithoutJre}}`.
* If Java (version 8 or higher) is not available on your computer, install it, and then run the Kojo installer again as shown above.
* After Kojo is installed, you can run it from the Desktop (if you opted for a Desktop shortcut), from the Development application category/group, or from the bin directory inside your Kojo install.
* The Kojo shortcut is named *Kojo Learning Environment*.

---

<h5 id="win">Windows</h5>

[Kojo Installer (64 bit exe)]({{ winInstaller }}) (Version: {{page.kojo_version}})

*Instructions:*
* Download the Kojo Installer (exe) (and make sure it is saved as a .exe file by your browser). Run it to install Kojo.
  * The above installer will only run on 64 bit Windows. If you are running 32 bit Windows, use the [cross-platform Kojo installer](/kojo-download#crossplatform).
  * If your anti-virus software does not let you install (or run) Kojo, follow [these instructions](http://wiki.kogics.net/sf:kojo-windows-antivirus) to get around the issue.
  * If you are running an old version of Windows 7 which has not been updated recently, you might run into an **installer error related to a missing dll**. In that case, use the [cross-platform Kojo installer](/kojo-download#crossplatform).
  * If you want to use Kojo on Windows XP, you will need to download and install *Java 8, Update 152* or earlier on your computer, and then use the [cross-platform Kojo installer](/kojo-download#crossplatform). If you need help with this, just [let us know](mailto:feedback@kogics..net).
* After Kojo is installed, you can run it from the Desktop (if you opted for a Desktop shortcut), or from the Windows Start Menu, via the *Kojo* Program Group.
* The Kojo shortcut is named *Kojo Learning Environment*.

---

<h5 id="mac">Mac</h5>

[Kojo Installer (dmg)]({{ macInstaller }}) (Version: {{page.kojo_version}})

*Instructions:*
* Download the Kojo Installer (dmg), open it, and run the installer that's inside to install Kojo. If the OS pops up a message about the installer, follow [these instructions](http://wiki.kogics.net/sf:kojo-dmg-damaged) to resolve the issue.
* After Kojo is installed, you can run it from the Desktop (if you opted for a Desktop shortcut), or from the directory (Applications, by default) where you installed it.

[Mac release notes](http://wiki.kogics.net/sf:kojo-mac-relnotes)

---

<h5 id="rpi">Raspberry Pi</h5>

[Kojo Installer (shell script)]({{ unixInstallerWithoutJre }}) (Version: {{page.kojo_version}}, needs Java 8, 11, or 17)

*Instructions:*
* Download the Kojo installer (shell script). Then run it by opening up a Terminal Window, going to the directory where the installer is located, and running:  sh Kojo_unix_2_9_26.sh
  * Java 8 comes pre-installed on the Raspberry Pi, and will be used by the Kojo installer above.
* After Kojo is installed, you can run it from the Desktop (if you opted for a Desktop shortcut), from the Programming application category/group, or from the bin directory inside your Kojo install.
* The Kojo shortcut is named Kojo Learning Environment.
* *Note* - you can hook up an Arduino with your Raspberry Pi and [drive the combo with Kojo](https://github.com/litan/kojo-arduino) for some hardware hacking fun.

---

<h5 id="chromebook">Chromebook</h5>

To install Kojo on Chromebooks, you need to:
* [Unlock your chromebook](http://www.androidauthority.com/crouton-turn-your-chromebook-into-far-more-than-a-glorified-web-browser-663044).
* And then install [Kojo for Linux/Unix](/kojo-download#unix) as described above.

---

<h5 id="crossplatform">Cross Platform</h5>

[Kojo Distribution (zip file)]({{ zipDistribution }}) (Version: {{page.kojo_version}}, needs Java 8, 11, or 17)

*Instructions:*
This is a fallback distribution, to be used if you run into problems with an installer that is specific to your platform. This distribution can be used on any platform where Java 8, 11, or 17 is supported. To install Kojo via this distribution:
* Make sure that Java 8, 11, or 17 is installed on your computer. If in doubt, get Java (version 8, 11, or 17) from a [Java download site](https://bell-sw.com/pages/downloads/?version=java).
* Download the Kojo Distribution (zip file) and extract it to a directory of your choice.
* To run Kojo:
  * On Windows - go into the bin directory under the Kojo directory and run the kojo.exe program (or kojo.cmd script) there to launch Kojo. For easier launching in the future, right click on kojo.exe and 'Send' it to the Desktop as a shortcut. You can then launch Kojo via the Desktop shortcut.
  * On Unix or Mac - go into the bin directory under the Kojo directory and run the kojo script there to launch Kojo. You can create a launcher for this script as appropriate for your platform and put the launcher on your Desktop.
* Note for advanced users - you are free to modify the kojo.cmd and kojo scripts to make them use a particular version of Java 8, 11, or 17; by default they use the Java that is available on the path, and will fail if this is not Java 8, 11, or 17.

---

<h5 id="media">Media Files</h5>

Media files can be used in games (and also as costumes for turtles). The Scratch Media Bundle is a good source for these files -- many different backgrounds, costumes, and sound files are available in the bundle. To use these files, download the media bundle zipfile and unzip it under your home directory. You can then access the media files from inside Kojo using their absolute path, or their path relative to your home directory. For more information, visit the [Media Notes page](http://wiki.kogics.net/sf:media-notes).

---

<h5 id="install4j">Installer Technology</h5>

The platform specific Kojo installers on this page have been built using the [Install4j multi-platform installer builder](https://www.ej-technologies.com/products/install4j/overview.html).

{% for i in (1..15) %}
<p>&nbsp;</p>
{% endfor %}