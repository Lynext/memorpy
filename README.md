# memorpy
This is a fixed fork of memorypy, a python library using ctypes to search/edit windows/linux/OSX/SunOS programs memory.

# install
```
pip install https://github.com/hrt/memorpy/archive/master.zip
```
# usage examples :
```python
>>> from memorpy import MemWorker, Process
>>> mem = MemWorker(name="Brawlhalla.exe")
>>> modules = mem.process.list_modules()
>>> print(modules)
{'COMDLG32.dll': 1971978240L, 'imagehlp.dll': 1978138624L, 'wow64.dll': 89980928L, 'MSWSOCK.dll': 1941504000L, 'msvcp_win.dll': 1989869568L, 'MSASN1.dll': 1987641344L, 'tier0_s.dll': 1876033536L, 'dwmapi.dll': 1952579584L, 'nvapi.dll': 1913061376L, 'cryptsp.dll': 1994194944L, 'DINPUT8.dll': 1912078336L, 'dbgcore.DLL': 1755447296L, 'iertutil.dll': 1790377984L, 'PROPSYS.dll': 1958543360L, 'SspiCli.dll': 1964113920L, 'advapi32.dll': 1987117056L, 'ole32.dll': 1996750848L, 'USER32.dll': 2005598208L, 'TextInputFramework.dll': 1819803648L, 'WINTRUST.dll': 1994326016L, 'WindowsCodecs.dll': 1746796544L, 'OLEACC.dll': 1810235392L, 'mlang.dll': 1750007808L, 'SHELL32.dll': 1978269696L, 'DNSAPI.dll': 1896153088L, 'WINMMBASE.dll': 1942093824L, 'HID.DLL': 1894973440L, 'MMDevApi.dll': 1824587776L, 'xinput1_4.dll': 1852833792L, 'WINMM.dll': 1943928832L, 'urlmon.dll': 1792671744L, 'NLAapi.dll': 1845624832L, 'dxgi.dll': 1912340480L, 'CRYPTBASE.dll': 1964048384L, 'ntdll.dll': 2007760896L, 'SETUPAPI.DLL': 1973551104L, 'sechost.dll': 1987837952L, 'Steam2.dll': 1568604160L, 'WININET.dll': 1936785408L, 'nvd3dum.dll': 1623654400L, 'rsaenh.dll': 1957298176L, 'PSAPI.DLL': 1966211072L, 'd2d1.dll': 1903755264L, 'IPHLPAPI.DLL': 1958281216L, 'napinsp.dll': 1845886976L, 'uxtheme.dll': 1949302784L, 'profapi.dll': 1971191808L, 'dhcpcsvc.DLL': 1952317440L, 'DSOUND.dll': 1821376512L, 'shcore.dll': 1965621248L, 'comctl32.dll': 1952907264L, 'winrnr.dll': 1845559296L, 'gpapi.dll': 1956970496L, 'MSCTF.dll': 1966276608L, 'VERSION.dll': 1955069952L, 'bcryptPrimitives.dll': 1973026816L, 'GDI32.dll': 1964244992L, 'CoreMessaging.dll': 1909063680L, 'WINSPOOL.DRV': 1960116224L, 'MSIMG32.dll': 1851588608L, 'steamclient.dll': 1825898496L, 'nvspcap.dll': 1621360640L, 'AVRT.dll': 1824194560L, 'gdi32full.dll': 1984299008L, 'CRYPT32.dll': 57147392L, 'steam.dll': 1688862720L, 'MessageBus.dll': 1925251072L, 'msvcrt.dll': 1990787072L, 'vstdlib_s.dll': 1867251712L, 'shlwapi.dll': 1989148672L, 'Windows.UI.dll': 1820393472L, 'Brawlhalla.exe': 1769472L, 'bcrypt.dll': 1987706880L, 'd3d9.dll': 1794506752L, 'OLEAUT32.dll': 1971322880L, 'XINPUT9_1_0.dll': 1941897216L, 'DnaManager.dll': 1566310400L, 'schannel.dll': 1690632192L, 'wintypes.dll': 1897988096L, 'mscms.dll': 1789198336L, 'USERENV.dll': 1952055296L, 'kernel.appcore.dll': 1978073088L, 'gameoverlayrenderer.dll': 1748369408L, 'd3d11.dll': 1898905600L, 'dcomp.dll': 1848705024L, 'clbcatq.dll': 1967587328L, 'wow64cpu.dll': 2007695360L, 'NSI.dll': 1987051520L, 'KERNELBASE.dll': 1994653696L, 'msi.dll': 1664155648L, 'twinapi.appcore.dll': 1909653504L, 'powrprof.dll': 1964441600L, 'd3dcompiler_47_32.dll': 1611005952L, 'RMCLIENT.dll': 1897857024L, 'RawData.dll': 1750335488L, 'dbghelp.dll': 1942290432L, 'nvldumd.dll': 1766260736L, 'CSERHelper.dll': 1688666112L, 'CoreUIComponents.dll': 1901199360L, 'AUDIOSES.DLL': 1822162944L, 'rasadhlp.dll': 1952251904L, 'pnrpnsp.dll': 1845755904L, 'wshbth.dll': 1845493760L, 'combase.dll': 1968570368L, 'ntmarta.dll': 1957494784L, 'cryptnet.dll': 1957101568L, 'cfgmgr32.dll': 2007302144L, 'fwpuclnt.dll': 1895759872L, 'KERNEL32.DLL': 1993277440L, 'Secur32.dll': 1952776192L, 'DEVOBJ.dll': 1852899328L, 'windows.storage.dll': 1997799424L, 'COMCTL32.dll': 1798111232L, 'WS2_32.dll': 1968177152L, 'NvCamera32.dll': 1614544896L, 'ColorAdapterClient.dll': 1809514496L, 'steam_api.dll': 1746534400L, 'Adobe AIR.dll': 1642070016L, 'dataexchange.dll': 1850146816L, 'win32u.dll': 2007564288L, 'wow64win.dll': 120258560L, 'RPCRT4.dll': 1964834816L, 'IMM32.DLL': 1988362240L, 'ucrtbase.dll': 1985806336L, 'inputhost.dll': 1911422976L, 'nvwgf2um.dll': 1576075264L, 'SteamAir.dll': 1689714688L}

>>> print(mem.Address(modules["Brawlhalla.exe"]).read())
9460301
```

In this example open a notepad.exe and type in some text we will edit from memory !
```python
>>> from memorpy import *
>>> mw=MemWorker(pid=3856) #you can also select a process by its name with the kwarg name=
>>> l=[x for x in mw.umem_search("hello")]
>>> l
[('', <Addr: 0x003287B0>)]
>>> a=l[0][1]
>>> a
<Addr: 0x003287B0>
>>> a+4
<Addr: 0x003287B4>
>>> print a
<Addr: 0x003287B0 : "h\x00e\x00l\x00l\x00o\x00 \x00t\x00h\x00i\x00s\x00 \x00i\x00s\x00 \x00a\x00 \x00m\x00e\x00s\x00s\x00a\x00g\x00e\x00 \x00I\x00" (bytes)>
>>> a.dump()
00328790: 46 00 72 00 61 00 6E 00 63 00 65 00 29 00 00 00  F.r.a.n.c.e.)...
003287A0: 00 00 00 00 00 00 00 00 F3 8F 57 0C 7F 6A 00 10  ..........W..j..
003287B0: 63 00 6F 00 75 00 63 00 6F 00 75 00 20 00 74 00  c.o.u.c.o.u. .t.
003287C0: 68 00 69 00 73 00 20 00 69 00 73 00 20 00 61 00  h.i.s. .i.s. .a.
003287D0: 20 00 6D 00 65 00 73 00 73 00 61 00 67 00 65 00   .m.e.s.s.a.g.e.
003287E0: 20 00 49 00 20 00 74 00 79 00 70 00 65 00 64 00   .I. .t.y.p.e.d.
003287F0: 20 00 69 00 6E 00 20 00 6E 00 6F 00 74 00 65 00   .i.n. .n.o.t.e.
00328800: 70 00 61 00 64 00 2E 00 65 00 78 00 65 00 20 00  p.a.d...e.x.e. .
00328810: 21 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  !...............
00328820: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
00328830: 00 00 00 00 04 00 27 00 F7 8F 74 2B 6A 6A 00 00  ......'...t+jj..
00328840: 30 7A 32 00 C0 8B 32 00 00 00 00 00 00 00 00 00  0z2...2.........
00328850: 01 00 01 00 01 01 00 00 00 00 00 00 00 00 00 00  ................
00328860: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
00328870: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
00328880: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
00328890: 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
003288A0: 01 00 00 01 00 00 01 00 00 00 00 01 00 00 00 00  ................
003288B0: 07 00 00 07 59 6A 00 00 B8 79 32 00 E8 35 32 00  ....Yj...y2..52.
003288C0: 50 54 9D ED E6 EB 55 42 82 89 F8 A3 1E 68 72 28  PT....UB.....hr(
003288D0: 03 00 00 03 7F 6A 00 00 C0 8B 32 00 E8 35 32 00  .....j....2..52.
003288E0: AA BA 43 9F 5C 80 8F 67 E2 8F 75 3F 6E 6A 00 0C  ..C.\..g..u?nj..
003288F0: F0 FE 30 00 70 FE 30 00 F0 FD 30 00 1D 17 ED 00  ..0.p.0...0.....
00328900: B6 8F 75 6B 7B 6A 00 08 00 00 00 00 00 00 00 00  ..uk{j..........
00328910: 11 10 0A 61 00 00 00 00 00 00 00 00 A0 00 00 00  ...a............
00328920: 0D 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
00328930: 00 00 80 41 00 00 80 41 00 00 80 3D 00 00 80 3D  ...A...A...=...=
00328940: 00 00 D0 00 00 00 30 00 1E FF 20 1F 00 00 00 00  ......0... .....
00328950: 71 80 0E 00 30 00 30 00 30 00 30 00 30 00 30 00  q...0.0.0.0.0.0.
00328960: 30 00 30 00 30 00 30 00 30 00 30 00 30 00 30 00  0.0.0.0.0.0.0.0.
00328970: 30 00 30 00 30 00 30 00 30 00 30 00 30 00 30 00  0.0.0.0.0.0.0.0.
00328980: 30 00 30 00 30 00 30 00 30 00 30 00 30 00 30 00 0.0.0.0.0.0.0.0.
>>> a.read(100).decode("utf-16-le")
u'hello this is a message I typed in notepad.exe !\x00\x00'
>>> a.write("pwned".encode("utf-16-le"))
1
>>> a.read(100).decode("utf-16-le")
u'pwned this is a message I typed in notepad.exe !\x00\x00'
```
Look back at your notepad and the text should be changed ! :)
A quicker way to do this could be :
```python
>>> mw.umem_replace("hello","pwned")
```

Some other interesting features like searching for different values types in memory and monitor their changes are also implemented through the Locator class. For example if you are looking to cheat in a game and you start with 200 ammo, you could do something like :

```python
>>> lo=Locator(mw)
>>> lo.feed(200)
...
<Addr: 0x0018FDE2>,
<Addr: 0x0018FDE4>,
<Addr: 0x0018FDE6>,
...]}
```
Use some ammo and "refeed" the locator (do this a couple of times until there is one result left)
```python
>>> lo.feed(199)
{'double': [],
 'float': [],
 'int': [<Addr: 0x0019FAF0>],
 'long': [],
 'short': [],
 'uint': [],
 'ulong': [],
 'ushort': []}
>>> a=_["int"][0]
>>> a.read()
199
>>>a.write(999999)
1
```
Now you have infinite ammo :o)


I hope this code will be useful to someone.

Have fun !
## Other examples
Have a look at [HattoriBot](https://github.com/hrt/HattoriBot) that has written a game hack using this fork

## Contact
by mail: contact@n1nj4.eu  
on Twitter: [Follow me on twitter](https://twitter.com/n1nj4sec)  

If some of you want to participate or send me a feedback, don't hesitate :-)  
  
This project is a personal development, please respect its philosophy don't use it for evil purpose !
