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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>UINT16</td>
<td><code>0x03</code></td>
<td>TransID</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UINT8</td>
<td><code>N/A</code></td>
<td>PacketType (see <a href="#">packet types</a>)</td>
</tr>
<tr>
<td>UINT32</td>
<td><code>N/A</code></td>
<td>IV</td>
</tr>
<tr>
<td>UINT32</td>
<td><code>N/A</code></td>
<td>CRC32</td>
</tr>
</tbody>
</table>

<p>ProbeBody:</p>

<table>
<thead>
<tr>
<th>Data type</th>
<th>Example</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>UINT8</td>
<td><code>N/A</code></td>
<td>PayLoadLen</td>
</tr>
</tr>
</thead>
<tbody>
<tr>
<td>UINT16</td>
<td><code>0xDA01</code></td>
<td>ProbeCMD (see <a href="#">packet types</a>)</td>
</tr>
<tr>
<td>UINT16</td>
<td><code>N/A</code></td>
<td>RequestID</td>
</tr>
<tr>
<td>UINT8</td>
<td><code>N/A</code></td>
<td>ParamListType</td>
</tr>
</tbody>
</table>
