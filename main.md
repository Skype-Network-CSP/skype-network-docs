<h1>Connecting to Server</h1>
<p>Skype uses UDP-supernode ports 33033 and TCP-supernode port 443 or 33033</p>

<h1>Skype Packet Structure</h1>
<p>The Skype protocol is binary, numbers use Big-Endian, then Little-Endian</p>

<table>
<thead>
<tr>
<th>Тип данных</th>
<th>Описание</th>
<th>Пример</th>
<th>Расшифровка</th>
</tr>
</thead>
<tbody>
<tr>
<td>UL</td>
<td>Четырёхбатовое число</td>
<td><code>1B 00 00 00</code></td>
<td>27</td>
</tr>
<tr>
<td>LPS</td>
<td>Строка, перед которой всегда идёт её длинна в формате UL</td>
<td><code>05 00 00 00 48 65 6C 6C 6F</code></td>
<td>Hello (длина 5)</td>
</tr>
</tbody>
</table>
