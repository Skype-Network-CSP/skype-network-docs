<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033</p>

<h1>Skype UDP Packet Structure</h1>
<p>The Skype protocol is binary, numbers use Big-Endian, then Little-Endian</p>
<p>When connected to a UDP super node, Skype sends a test request to verify the node, which looks like this:</p>

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
<td><code>N/A</code></td>
<td>TransID</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td><code>N/A</code></td>
<td>PacketType (see <a href="#">packet types</a>)</td>
</tr>
<tr>
<td>UL</td>
<td><code>N/A</code></td>
<td>IV</td>
</tr>
<tr>
<td>UL</td>
<td><code>N/A</code></td>
<td>CRC32</td>
</tr>
</tbody>
</table>
