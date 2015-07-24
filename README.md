# **Qt5-MSVC-Static**

Set of tools to build Qt5 static libs on Windows.

**Description**

This tools copies a modified mkspec config in the qtbase repo to build a static library.

**Dependencies**

 - Python (https://www.python.org/downloads/windows/)
 - Perl (http://strawberryperl.com/)
 - Git (https://msysgit.github.io/)
 - OpenSSL (http://slproweb.com/download/Win32OpenSSL-1_0_2d.exe)
 - ICU (http://www.npcglib.org/~stathis/downloads/icu-55.1-vs2012.7z)

Make sure *Python*, *Perl* and *Git* are all in the *PATH*.

You can check the official documentation here: 
http://doc.qt.io/qt-5/windows-requirements.html
http://doc.qt.io/qt-5/windows-building.html

**Usage**

You will need to run *setup.bat* from the VS command tool.
Run *setup.bat*, then *nmake* and finally *nmake install*.

**Configuration**

Only release libs are enabled by default. 
You can add the debug libs or use the official sdk libs for debugging.

By default I only enabled a rather restricted set of modules.
Here is the config output:

    QMAKESPEC...................win32-msvc2012 (commandline)
	Architecture................i386, features: sse sse2
	Host Architecture...........i386, features: sse sse2
	Maketool....................nmake
	Debug.......................no
	Force debug info............no
	C++11 support...............auto
	Link Time Code Generation...no
	Accessibility support.......no
	RTTI support................yes
	SSE2 support................yes
	SSE3 support................yes
	SSSE3 support...............yes
	SSE4.1 support..............yes
	SSE4.2 support..............yes
	AVX support.................yes
	AVX2 support................yes
	NEON support................no
	OpenGL support..............yes
	Large File support..........yes
	NIS support.................no
	Iconv support...............no
	Evdev support...............no
	Mtdev support...............no
	Inotify support.............no
	eventfd(7) support..........no
	Glib support................no
	CUPS support................no
	OpenVG support..............no
	SSL support.................yes
	OpenSSL support.............yes
	libproxy support............no
	Qt D-Bus support............no
	Qt Widgets module support...yes
	Qt GUI module support.......yes
	QML debugging...............yes
	DirectWrite support.........no
	Use system proxies..........no
	
	QPA Backends:
	    GDI.....................yes
	    Direct2D................no
	
	Third Party Libraries:
	    ZLIB support............qt
	    GIF support.............yes
	    JPEG support............yes
	    PNG support.............yes
	    FreeType support........yes
	    Fontconfig support......no
	    HarfBuzz support........qt
	    PCRE support............qt
	    ICU support.............yes
	    ANGLE...................no
	    Dynamic OpenGL..........yes
	
	Styles:
	    Windows.................yes
	    Windows XP..............yes
	    Windows Vista...........yes
	    Fusion..................yes
	    Windows CE..............no
	    Windows Mobile..........no
	
	Sql Drivers:
	    ODBC....................no
	    MySQL...................no
	    OCI.....................no
	    PostgreSQL..............no
	    TDS.....................no
	    DB2.....................no
	    SQLite..................yes (qt)
	    SQLite2.................no
	    InterBase...............no

You can check the official configuration guide here:
http://doc.qt.io/qt-5/configure-options.html
