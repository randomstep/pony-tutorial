# Mac OSX
First, install [homebrew](http://brew.sh/) if you haven't already.

Make sure to have the newest ```brew``` formulas from ```homebrew:master```:

```bash
$ brew update
```

Then, install ponyc:

```bash
$ brew install ponyc
```
# Linux

Installers for various distributions to supply precompiled binaries are available. All linux installers are signed with the public key published [here](http://ponylang.org/releases/buildbot@lists.ponylang.org.gpg.key).

## Available packages

* ```ponyc```: Recommended. Should work on most modern ```x86_64``` platforms.
* ```ponyc-avx2```: For platforms with AVX2 support.

## Apt-get and Aptitude

First, to avoid warnings about an untrusted repository, you can trust ```ponylang.org```:

```bash
$ wget -O - http://www.ponylang.org/releases/buildbot@lists.ponylang.org.gpg.key | sudo apt-key add -
```

**Option 1:** Install ```python-software-properties``` (Debian Wheezy and earlier, Ubuntu) or ```software-properties-common``` (Debian Jessy and later) for ```add-apt-repository```. Then, add the ponylang.org repository:

```bash
$ sudo add-apt-repository "deb http://ponylang.org/releases/apt ponyc main"
$ sudo add-apt-repository "deb http://ponylang.org/releases/apt ponyc-avx2 main"
```

**Option 2**: Manually add the following three lines to your ```sources.list``` (```/etc/apt/sources.list``` on Ubuntu, and ```/etc/apt-get/sources.list``` on Debian):

```bash
deb http://ponylang.org/releases/apt ponyc main
deb http://ponylang.org/releases/apt ponyc-avx2 main
```
Then, update your repository cache:

```bash
$ sudo apt-get update
```

Install ```ponyc``` or ```ponyc-avx2```

```bash
$ sudo apt-get install <package name>
```

## Zypper

First, add the ponylang.org repository:

```bash
$ sudo zypper ar -f http://www.ponylang.org/releases/yum/ponyc.repo
```

Install ```ponyc``` or ```ponyc-avx2```:

```bash
$ sudo zypper install <package-name>
```

## YUM

First, add the ponylang.org repository:

```bash
$ sudo yum-config-manager --add-repo=http://www.ponylang.org/releases/yum/ponyc.repo
```

**Alternatively**, if ```yum-config-manager``` is not available on your system, you can add the repository manually:

```bash
$  sudo wget -O /etc/yum.repos.d/ponyc.repo http://www.ponylang.org/releases/yum/ponyc.repo
```

Install ```ponyc``` or ```ponyc-avx2```:

```bash
$ sudo yum install <package-name>
```

# Windows

64-Bit installers for Windows 7, 8, 8.1 and 10 will be available soon.

## Did it work?

Running the following command should now display the installed version of ```ponyc```:

```bash
$ ponyc --version
0.1.6
```

# Downloads
All installers can also be downloaded from ponylang.org's servers:

* [Ubuntu/Debian](http://ponylang.org/releases/debian)
* [RPM](http://ponylang.org/releases/yum)
* [Windows](http://ponylang.org/releases/windows)
