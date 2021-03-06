---
title: Status of QNAP TS-41x/TS-42x support
nav: Status
description: Status of QNAP QNAP TS-41x/TS-42x support in Debian
keywords: [Debian, QNAP, TS-410, TS-410U, TS-412, TS-419P, TS-419U, TS-420, TS-421, support, status]
---

<% content_for :right do %>
<img src = "../images/r_qnap_ts419p.jpg" class="border" alt="QNAP TS-419P from the front" width="148" height="148" />

<%= render "adsense-wideskyscaper-right" %>
<% end %>

<h1>Status of QNAP TS-410, TS-410U, TS-412, TS-419P, TS-419P+, TS-419P II, TS-419U, TS-410U+, TS-420 and TS-421</h1>

QNAP TS-41x/TS-42x devices are based on a Marvell Kirkwood System on a Chip.
Marvell has done a lot of work to get support for the Kirkwood platform
into the mainline kernel.  However, some features of the Kirkwood platform
are not as well supported in the mainline kernel (which we use in Debian)
as in the original Marvell LSP (Linux Support Package) used by QNAP.
Please take this into account before deciding whether you want to install
Debian, especially if you have specific requirements (e.g. related to
performance).

The table below shows how well different components of the QNAP
TS-41x/TS-42x are supported by Debian:

<table>

<tr>
<th>Component</th>
<th>Comment</th>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">Debian</td>
<td>Debian and the Debian installer work well</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">CPU</td>
<td>Supported in the kernel by the `kirkwood` platform</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">SATA</td>
<td>Supported in the kernel by the `sata_mv` module</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">Ethernet</td>
<td>Supported in the kernel by the `mv643xx` module</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">USB</td>
<td>Supported</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">RTC</td>
<td>Supported in the kernel by the `rtc-s35390a` module</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">LEDs</td>
<td>Supported in qcontrol</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">LCD</td>
<td>Supported in qcontrol; you have to <a href="../tips/#qcontrol-upgrade">install
the qcontrol backport</a></td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">Fan</td>
<td>Supported in qcontrol; you can <a href="../tips/#qcontrol-upgrade">upgrade
qcontrol</a> to get automatic temperature regulation.</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">Beeper</td>
<td>Supported in qcontrol</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">XOR engine</td>
<td>Supported</td>
</tr>

<tr>
<td style="color: black; background-color: #FFFF00">Crypto engine</td>
<td>Basic support</td>
</tr>

<tr>
<td style="color: white; background-color: #AA0000">Wake-on-LAN (WOL)</td>
<td>Not supported.  Support has recently been added upstream so this will
appear in Debian in the future</td>
</tr>

<tr>
<td style="color: white; background-color: #00AA00">Scheduled power</td>
<td>Supported; see <a href = "../tips/#wakealarm">instructions</a></td>
</tr>

</table>

<div class="bbf">
<%= render "adsense-banner-before-footer" %>
</div>

