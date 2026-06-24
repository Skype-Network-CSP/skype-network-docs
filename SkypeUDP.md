<h1>Skype UDP SuperNode</h1>
<p>Skype uses port 33033 for the UDP supernode, it sends a Probe request to verify the node:</p>
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
    <td><code>0xDA01</code></td>
    <td>ProbeCMD (see <a href="#">cmd list</a>)</td>
</tr>
<tr>
    <td>UINT16</td>
    <td><code>N/A</code></td>
    <td>RequestID</td>
</tr>
<tr>
    <td>UINT8</td>
    <td><code>0x42</code></td>
    <td>ParamListType</td>
</tr>
<tr>
    <td>UINT8</td>
    <td><code>N/A</code></td>
    <td>NbObj</td>
</tr>
</tbody>
</table>

<p>ProbeBody is encrypted in RC4, encryption will be described in the future.</p>
