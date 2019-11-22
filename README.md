# sql-java-kerberos

```
$ mvn exec:java -D"exec.mainClass"="org.acme.KerberosTestBase"
[INFO] Scanning for projects...
[INFO] 
[INFO] ---------------------< org.acme:sql-java-kerberos >---------------------
[INFO] Building sql-java-kerberos 1.0.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- exec-maven-plugin:1.6.0:java (default-cli) @ sql-java-kerberos ---
>>>KinitOptions cache name is /tmp/krb5cc_1000
>>>DEBUG <CCacheInputStream>  client principal is MSSQLSvc/msql.example.com:1433@EXAMPLE.COM
>>>DEBUG <CCacheInputStream> server principal is krbtgt/EXAMPLE.COM@EXAMPLE.COM
>>>DEBUG <CCacheInputStream> key type: 18
>>>DEBUG <CCacheInputStream> auth time: Fri Nov 22 12:38:21 AEST 2019
>>>DEBUG <CCacheInputStream> start time: Fri Nov 22 12:38:21 AEST 2019
>>>DEBUG <CCacheInputStream> end time: Sat Nov 23 00:38:21 AEST 2019
>>>DEBUG <CCacheInputStream> renew_till time: Fri Nov 29 12:38:21 AEST 2019
>>> CCacheInputStream: readFlags()  FORWARDABLE; RENEWABLE; INITIAL; PRE_AUTH;
>>>DEBUG <CCacheInputStream>  client principal is MSSQLSvc/msql.example.com:1433@EXAMPLE.COM
>>>DEBUG <CCacheInputStream> server principal is krb5_ccache_conf_data/fast_avail/krbtgt/EXAMPLE.COM@EXAMPLE.COM@X-CACHECONF:
>>>DEBUG <CCacheInputStream> key type: 0
>>>DEBUG <CCacheInputStream> auth time: Thu Jan 01 10:00:00 AEST 1970
>>>DEBUG <CCacheInputStream> start time: null
>>>DEBUG <CCacheInputStream> end time: Thu Jan 01 10:00:00 AEST 1970
>>>DEBUG <CCacheInputStream> renew_till time: null
>>> CCacheInputStream: readFlags() 
>>>DEBUG <CCacheInputStream>  client principal is MSSQLSvc/msql.example.com:1433@EXAMPLE.COM
>>>DEBUG <CCacheInputStream> server principal is krb5_ccache_conf_data/pa_type/krbtgt/EXAMPLE.COM@EXAMPLE.COM@X-CACHECONF:
>>>DEBUG <CCacheInputStream> key type: 0
>>>DEBUG <CCacheInputStream> auth time: Thu Jan 01 10:00:00 AEST 1970
>>>DEBUG <CCacheInputStream> start time: null
>>>DEBUG <CCacheInputStream> end time: Thu Jan 01 10:00:00 AEST 1970
>>>DEBUG <CCacheInputStream> renew_till time: null
>>> CCacheInputStream: readFlags() 
get normal credential
Java config name: /home/mike/git/sql-java-kerberos/src/main/resources/krb5.conf
Loaded from Java config
Found ticket for MSSQLSvc/msql.example.com:1433@EXAMPLE.COM to go to krbtgt/EXAMPLE.COM@EXAMPLE.COM expiring on Sat Nov 23 00:38:21 AEST 2019
Entered Krb5Context.initSecContext with state=STATE_NEW
Found ticket for MSSQLSvc/msql.example.com:1433@EXAMPLE.COM to go to krbtgt/EXAMPLE.COM@EXAMPLE.COM expiring on Sat Nov 23 00:38:21 AEST 2019
Service ticket not found in the subject
>>> Credentials acquireServiceCreds: same realm
default etypes for default_tgs_enctypes: 18 17 23.
>>> CksumType: sun.security.krb5.internal.crypto.RsaMd5CksumType
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
>>> KdcAccessibility: reset
>>> KrbKdcReq send: kdc=kerberos.example.com TCP:8888, timeout=30000, number of retries =3, #bytes=726
>>> KDCCommunication: kdc=kerberos.example.com TCP:8888, timeout=30000,Attempt =1, #bytes=726
>>>DEBUG: TCPClient reading 725 bytes
>>> KrbKdcReq send: #bytes read=725
>>> KdcAccessibility: remove kerberos.example.com:8888
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
default etypes for default_tgs_enctypes: 18 17 23.
>>> CksumType: sun.security.krb5.internal.crypto.RsaMd5CksumType
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
>>> KrbKdcReq send: kdc=kerberos.example.com TCP:8888, timeout=30000, number of retries =3, #bytes=714
>>> KDCCommunication: kdc=kerberos.example.com TCP:8888, timeout=30000,Attempt =1, #bytes=714
>>>DEBUG: TCPClient reading 700 bytes
>>> KrbKdcReq send: #bytes read=700
>>> KdcAccessibility: remove kerberos.example.com:8888
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
>>> KrbApReq: APOptions are 00100000 00000000 00000000 00000000
>>> EType: sun.security.krb5.internal.crypto.Aes256CtsHmacSha1EType
Krb5Context setting mySeqNumber to: 451333052
Created InitSecContextToken:
0000: 01 00 6E 82 05 4E 30 82   05 4A A0 03 02 01 05 A1  ..n..N0..J......
0010: 03 02 01 0E A2 07 03 05   00 20 00 00 00 A3 82 01  ......... ......
0020: 7C 61 82 01 78 30 82 01   74 A0 03 02 01 05 A1 0D  .a..x0..t.......
0030: 1B 0B 45 58 41 4D 50 4C   45 2E 43 4F 4D A2 2C 30  ..EXAMPLE.COM.,0
0040: 2A A0 03 02 01 00 A1 23   30 21 1B 08 4D 53 53 51  *......#0!..MSSQ
0050: 4C 53 76 63 1B 15 6D 73   71 6C 2E 65 78 61 6D 70  LSvc..msql.examp
0060: 6C 65 2E 63 6F 6D 3A 31   34 33 33 A3 82 01 2E 30  le.com:1433....0
0070: 82 01 2A A0 03 02 01 12   A1 03 02 01 02 A2 82 01  ..*.............
0080: 1C 04 82 01 18 EF 27 85   5F 86 17 4F 07 8E AC 9D  ......'._..O....
0090: E6 02 41 1F CD F1 FF 18   1F 4E 1B 87 C8 95 47 20  ..A......N....G 
00A0: 1F 4E CB DD 4B D2 68 F9   60 A4 08 20 D4 6F 66 B7  .N..K.h.`.. .of.
00B0: BC 78 77 62 40 1F 40 39   A9 B1 63 AE 7B 08 55 9F  .xwb@.@9..c...U.
00C0: 36 B7 E4 E2 F0 4E 47 38   68 64 58 07 EF B5 E6 52  6....NG8hdX....R
00D0: FA A4 D9 D8 3C 1B 8D 64   A0 0B 61 0B 06 44 F9 84  ....<..d..a..D..
00E0: 66 6A AA E2 32 0E B7 A1   2B 82 0D 37 01 FD B3 FA  fj..2...+..7....
00F0: 2A E4 C1 5C D3 05 45 49   F7 7A CB 7F 0C E5 4E C7  *..\..EI.z....N.
0100: A8 75 47 E9 8D D7 5B 40   0E F0 9A 6B 18 42 A0 3C  .uG...[@...k.B.<
0110: EE 5A 2D 29 F0 E7 22 B0   26 2F 5A 5C 3D 6E BD 59  .Z-)..".&/Z\=n.Y
0120: 0F F8 95 E0 86 13 04 7F   0B EE A6 46 A6 63 E0 45  ...........F.c.E
0130: 12 F4 BA 55 AA A6 CA FB   72 0F 49 5D BE 01 D5 96  ...U....r.I]....
0140: C7 32 1D ED 5B B0 E7 3B   75 E0 8B EE 87 A6 BB C5  .2..[..;u.......
0150: 33 2A E8 BF F4 12 6A 9F   9A 6E 5E 50 B7 E3 5E 37  3*....j..n^P..^7
0160: C2 FC 1A 2D 83 5C 68 48   33 EB B1 D4 A6 0C 43 DE  ...-.\hH3.....C.
0170: EE 37 F6 98 74 3B FB B4   16 55 A2 58 18 0F 70 59  .7..t;...U.X..pY
0180: ED 6D 20 22 F1 9A 5D 50   75 DB BE 7F E4 4C CA A6  .m "..]Pu....L..
0190: 89 55 4C 78 F6 7E F5 1D   89 09 5B 78 F7 A4 82 03  .ULx......[x....
01A0: B3 30 82 03 AF A0 03 02   01 12 A2 82 03 A6 04 82  .0..............
01B0: 03 A2 C0 8F 2E 4E E5 39   99 EC 85 DE 95 4B 73 28  .....N.9.....Ks(
01C0: 03 23 7F 59 4B CE 3F 89   26 1F A3 22 50 61 D4 A2  .#.YK.?.&.."Pa..
01D0: F9 C3 22 23 2F 62 40 FC   A6 40 2B 28 E2 A9 51 50  .."#/b@..@+(..QP
01E0: 0A 58 03 A8 E7 33 3A 95   89 CB 15 AC 9A 61 E0 B9  .X...3:......a..
01F0: FA E2 33 69 A4 67 B7 44   A1 C0 75 0F 2B 27 A2 04  ..3i.g.D..u.+'..
0200: 98 90 48 EC 52 BC 48 A2   5D 35 0A 15 BA 94 18 E6  ..H.R.H.]5......
0210: D7 58 B5 BF 17 A6 99 E2   AF D2 45 76 B9 53 2A 0C  .X........Ev.S*.
0220: 8A 85 D8 DA 63 EF 6A 7C   68 40 DF 41 4E 39 0F E4  ....c.j.h@.AN9..
0230: 71 57 0F 01 D3 80 79 1D   F9 85 92 12 B8 AD 98 F7  qW....y.........
0240: 4C 1D FC 3F 20 E2 AD 2B   07 87 E7 D2 CE E7 C8 9E  L..? ..+........
0250: 85 DF E6 91 B5 A2 8A 12   9F 51 5D F6 C0 1B 84 6B  .........Q]....k
0260: BC 56 1A EB 95 65 48 99   18 9B 86 BE DB AD 95 8F  .V...eH.........
0270: 68 E8 5F A4 1F 7C F4 8D   9E 18 70 21 AB 4A 4B 90  h._.......p!.JK.
0280: EC C3 C0 14 7E 0B DE AA   BB 22 DD 3F 08 DF 48 55  .........".?..HU
0290: 59 97 1E F4 B6 DA 1A 8D   EE B5 FD EC 69 E6 B7 DB  Y...........i...
02A0: 2C 1B FB E2 F4 B2 0D 2B   9A CB 13 F7 4A 0E 7D 33  ,......+....J..3
02B0: 20 A5 42 C7 21 B6 6F 3C   A0 ED 8F C0 17 73 72 61   .B.!.o<.....sra
02C0: 19 43 19 44 F6 B2 E8 91   A9 50 0E B6 B1 F6 52 A9  .C.D.....P....R.
02D0: BF A2 B4 BA 90 22 CC CB   37 77 2E 02 0D BF B6 F0  ....."..7w......
02E0: 83 E7 71 27 55 81 31 9C   1C CC D1 AF D0 F1 B5 92  ..q'U.1.........
02F0: 2D 92 A5 3E 02 42 EA 40   18 83 EB D8 17 D6 EC 79  -..>.B.@.......y
0300: F1 1E E3 91 64 3F 9D 87   6E 89 04 0D BD 80 29 1B  ....d?..n.....).
0310: 2D C6 82 C1 BE 89 6E DA   22 45 33 61 96 79 61 31  -.....n."E3a.ya1
0320: 3E 7D 6E 2B 29 7C 7E CF   CE BD 2A EE 3F 8C 76 35  >.n+).....*.?.v5
0330: 7E F4 CA 1C 65 F2 90 BB   AB DF DD 45 27 BB AC A5  ....e......E'...
0340: 2C 6A 66 A0 D0 3D 22 A9   BF 15 96 69 55 96 FA 96  ,jf..="....iU...
0350: 30 B4 F5 5A 8E 1F AB 42   45 35 2C 30 4F 10 3C DA  0..Z...BE5,0O.<.
0360: 7F B5 A6 C1 B9 FA 3F B8   94 DA 3E 3F 11 28 FA 57  ......?...>?.(.W
0370: 1B 32 51 0C FC 40 6F 7A   56 32 D7 21 0A 9E A5 20  .2Q..@ozV2.!... 
0380: 2A 8C 31 09 1D EB 51 15   9D BF 5B 2E 6B 00 C2 7A  *.1...Q...[.k..z
0390: 96 F3 3C EC 17 19 B2 3F   9C A0 D8 F3 27 1E 56 8B  ..<....?....'.V.
03A0: 56 96 B8 D7 56 D1 49 6F   A7 11 12 4F 65 4D 15 22  V...V.Io...OeM."
03B0: 51 78 9E 1C FE 39 74 3E   B5 31 09 BC 21 60 B9 6B  Qx...9t>.1..!`.k
03C0: 6B FA 06 EC 52 D3 36 20   53 D3 36 21 6D 59 8A A1  k...R.6 S.6!mY..
03D0: DB 7E 30 9B 5F 6C 05 A0   BF 62 94 39 52 2F A5 E6  ..0._l...b.9R/..
03E0: DB DE 39 D1 A9 C4 FF 85   47 9F C6 7B 89 D0 5C 3D  ..9.....G.....\=
03F0: B8 19 A7 48 91 53 8B 3E   0A 79 4C CD DE EF 12 D9  ...H.S.>.yL.....
0400: A7 99 F0 04 B2 B6 FA A4   EF EA 25 7A BC D9 68 19  ..........%z..h.
0410: 50 15 25 2F 90 E0 B6 E1   62 95 A8 1A EF 8C C3 D9  P.%/....b.......
0420: 56 F4 9C E5 87 18 AB CA   52 F8 62 A6 E3 E6 C4 53  V.......R.b....S
0430: 9F EE 8D EF D3 78 8E E1   E4 38 F2 16 F2 72 C2 2C  .....x...8...r.,
0440: 5D D4 87 10 D9 72 ED 2C   A2 55 0E 92 53 F5 CA BD  ]....r.,.U..S...
0450: E7 97 73 50 9E 36 3C D5   80 EF 8A 7D 55 2E AA 56  ..sP.6<.....U..V
0460: DA 4A 42 C3 4D 3D CF C1   2C 4B EF 12 31 F0 F7 5C  .JB.M=..,K..1..\
0470: 8F 25 01 FA 0E 1A C8 97   75 CF 7C 0A FB EE C4 BF  .%......u.......
0480: B4 C9 AF 8D 78 3B 40 50   55 9E 3A 22 A8 7A 39 B4  ....x;@PU.:".z9.
0490: 53 BA BB 3F 1E BD 53 2F   85 0F 32 05 2C 84 E7 DA  S..?..S/..2.,...
04A0: 3C 55 C2 35 2F 95 AB 79   EF 33 E4 19 2C A0 F2 B7  <U.5/..y.3..,...
04B0: 00 AA 29 7D E8 73 30 AE   67 04 18 86 83 67 62 FD  ..)..s0.g....gb.
04C0: 64 F1 51 75 0C 65 35 BF   C7 DD FF 64 E4 F1 18 16  d.Qu.e5....d....
04D0: 6F 94 82 E8 15 E4 51 B4   E1 46 A9 79 09 EC 70 8E  o.....Q..F.y..p.
04E0: E3 98 AC 55 C9 87 9C D7   F9 7E 2F B8 8A FD 70 49  ...U....../...pI
04F0: AB E7 5C BB 2F 42 B9 86   5D 62 18 97 85 1A A9 29  ..\./B..]b.....)
0500: AC DD A9 E5 E1 97 C6 CE   23 AB 0A 6E B4 E1 86 8B  ........#..n....
0510: 69 2A D3 6C C8 60 36 4A   62 7E 88 1F A3 37 D6 70  i*.l.`6Jb....7.p
0520: 0D 9A F9 A6 93 2A 39 8B   E4 51 2B 1A C5 0D 35 AA  .....*9..Q+...5.
0530: 11 9B 6C 81 2E 6D 1F 1F   55 0B 74 2E E6 F2 54 4A  ..l..m..U.t...TJ
0540: C3 C0 67 59 DA E0 80 57   63 2B F6 23 2D 20 E2 92  ..gY...Wc+.#- ..
0550: C4 E9 08 E5                                        ....

Service ticket generated, JAVA works!
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 0.743 s
[INFO] Finished at: 2019-11-22T12:38:49+10:00
[INFO] ------------------------------------------------------------------------
```
