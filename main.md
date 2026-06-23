<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033</p>

<h1>Skype UDP Packet Structure</h1>
<p>The Skype protocol is binary, numbers use Big-Endian, then Little-Endian</p>
<p>When connected to a UDP-supernode, Skype sends a test request to verify the node which looks like this:</p>
<p>ProbeHeader:</p>
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
<td>UINT32</td>
<td><code>N/A</code></td>
<td>TransID (2 bytes)</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UINT32</td>
<td><code>N/A</code></td>
<td>PacketType ( 1 byte, see <a href="#">packet types</a>)</td>
</tr>
<tr>
<td>UINT32</td>
<td><code>N/A</code></td>
<td>IV (4 bytes)</td>
</tr>
<tr>
<td>UINT32</td>
<td><code>N/A</code></td>
<td>CRC32 (4 bytes)</td>
</tr>
</tbody>
</table>
<p>ProbeBody:</p>
