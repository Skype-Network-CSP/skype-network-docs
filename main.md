<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033.</p>
<p>Earlier versions of Skype (1.x–5.x) used the Event Server to exchange data between the client and the server (contacts, statuses, messages).</p>
<p>Later, Skype switched to the <strong>MSNP24</strong> protocol — the same protocol used by <strong>Windows Live Messenger</strong>.</p>

<h1>Skype UDP Packet Structure</h1>
<p>The Skype protocol is binary. Numbers use Big-Endian for the header, then Little-Endian for the encrypted body.</p>
<p>When connected to a UDP-supernode, Skype sends a test request to verify the node which looks like this:</p>

<h2>ProbeHeader:</h2>

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
    <td><code>N/A</code></td>
    <td>TransID</td>
</tr>
<tr>
    <td>UINT8</td>
    <td><code>0x03</code></td>
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

<h2>ProbeBody:</h2>

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
<tr>
    <td>UINT16</td>
    <td><code>01 DA</code></td>
    <td>ProbeCMD (see <a href="#">cmd list</a>)</td>
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
<tr>
    <td>UINT8</td>
    <td><code>0x01</code></td>
    <td>NbObj</td>
</tr>
</tbody>
</table>

<p>ProbeBody is encrypted in RC4, encryption will be described in the future.</p>
