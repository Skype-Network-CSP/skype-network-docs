<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033</p>

<h1>Skype UDP Packet Structure</h1>
<p>The Skype protocol is binary, numbers use Big-Endian, then Little-Endian</p>

<table>
<thead>
<tr>
<th>Data type</th>
<th>Description</th>
<th>Example</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td>Packet Transaction ID</td>
<td><code>02 01</code></td>
<td>TransID</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td><code>03</code></td>
<td>PacketType</td>
</tr>
</tbody>
</table>
