---
title: Protocol Rendering
description: Example of protocol rendering bit tables
protocol_rendering: true
---
# Protocol Rendering

<a class="button" href="https://msdn.microsoft.com/en-us/library/c9876f5a-664b-46a3-9887-ba63f113abf5">MSDN</a>

<p>Unicode:</p>

## Bit Table

<table>
 <tr>
 <th><p><br>0</p></th>
 <th><p><br>1</p></th>
 <th><p><br>2</p></th>
 <th><p><br>3</p></th>
 <th><p><br>4</p></th>
 <th><p><br>5</p></th>
 <th><p><br>6</p></th>
 <th><p><br>7</p></th>
 <th><p><br>8</p></th>
 <th><p><br>9</p></th>
 <th><p>1<br>0</p></th>
 <th><p><br>1</p></th>
 <th><p><br>2</p></th>
 <th><p><br>3</p></th>
 <th><p><br>4</p></th>
 <th><p><br>5</p></th>
 <th><p><br>6</p></th>
 <th><p><br>7</p></th>
 <th><p><br>8</p></th>
 <th><p><br>9</p></th>
 <th><p>2<br>0</p></th>
 <th><p><br>1</p></th>
 <th><p><br>2</p></th>
 <th><p><br>3</p></th>
 <th><p><br>4</p></th>
 <th><p><br>5</p></th>
 <th><p><br>6</p></th>
 <th><p><br>7</p></th>
 <th><p><br>8</p></th>
 <th><p><br>9</p></th>
 <th><p>3<br>0</p></th>
 <th><p><br>1</p></th>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwMagic</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwCRCPartial</p>
 </td>
 </tr>
 <tr>
 <td colspan="16">
 <p>wMagicClient</p>
 </td>
 <td colspan="16">
 <p>wVer</p>
 </td>
 </tr>
 <tr>
 <td colspan="16">
 <p>wVerClient</p>
 </td>
 <td colspan="8">
 <p>bPlatformCreate</p>
 </td>
 <td colspan="8">
 <p>bPlatformAccess</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwReserved1</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwReserved2</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>bidUnused</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>bidNextP</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwUnique</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>rgnid[]
 (128 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>qwUnused</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>root
 (72 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwAlign</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>root
 (72 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>rgbFM
 (128 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>rgbFP
 (128 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="8">
 <p>bSentinel</p>
 </td>
 <td colspan="8">
 <p>bCryptMethod</p>
 </td>
 <td colspan="16">
 <p>rgbReserved</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>bidNextB</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>dwCRCFull</p>
 </td>
 </tr>
 <tr>
 <td colspan="24">
 <p>rgbReserved2</p>
 </td>
 <td colspan="8">
 <p>bReserved</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>rgbReserved3
 (32 bytes)</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
 <tr>
 <td colspan="32">
 <p>...</p>
 </td>
 </tr>
</table>

## Normal Table


|Column1  |Column2  |Column3  |
|---------|---------|---------|
|1     |🥧|🥧|
|2     |🥧|🥧|
|3     |🥧|🥧|
|4     |🥧|🥧|
|5     |🥧|🥧|
|6     |🥧|🥧|
|     |🥧|🥧|
|8     |🥧|🥧|
