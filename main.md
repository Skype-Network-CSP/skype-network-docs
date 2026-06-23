<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033</p>

<h1>Skype UDP Packet Structure</h1>
<p>The Skype protocol is binary, numbers use Big-Endian, then Little-Endian</p>

<table>
<thead>
<tr>
<th>Data type</th>
<th>Example</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td><code>0x0100</code></td>
<td>TransID</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td><code>0x03</code></td>
<td>PacketType (see <a href="#">packet types</a>)</td>
</tr>
</tbody>
</table>
