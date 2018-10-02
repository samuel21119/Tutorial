# 補充

## C++其餘運算子與結合順序

<table>
  <thead>
    <tr>
      <th style="text-align:left">順序</th>
      <th style="text-align:left">運算子</th>
      <th style="text-align:left">結合規則</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left"><code>::</code>
      </td>
      <td style="text-align:left">無</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left"><code>()</code>
        <br /><code>[]</code>
        <br /><code>-&gt;</code>
        <br /><code>.</code>
        <br /><code>++ --</code> (後綴)</td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left"><code>!</code>
        <br /><code>~</code>
        <br /><code>++ --</code> (後綴)
        <br /><code>+ - </code>(正負號，一元運算子)
        <br /><code>*</code>
        <br /><code>&amp;</code>
        <br /><code>(type)</code>
        <br /><code>sizeof</code>
      </td>
      <td style="text-align:left">右至左</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">
        <p><code>.*</code>
        </p>
        <p><code>&#x2013;&gt;*</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">
        <p><code>*</code>
        </p>
        <p><code>/</code>
        </p>
        <p><code>%</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">
        <p><code>+</code>
        </p>
        <p><code>-</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">
        <p><code>&lt;&lt;</code>
        </p>
        <p><code>&gt;&gt;</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">
        <p><code>&lt;</code>
        </p>
        <p><code>&gt;</code>
        </p>
        <p><code>&lt;=</code>
        </p>
        <p><code>&gt;=</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">
        <p><code>==</code>
        </p>
        <p><code>!=</code>
        </p>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left"><code>&amp;</code>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left"><code>^</code>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left"><code>|</code>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left"><code>&amp;&amp;</code>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left"><code>||</code>
      </td>
      <td style="text-align:left">左至右</td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left"><code>? : </code>(三元條件式)</td>
      <td style="text-align:left">右至左</td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">
        <p><code>=</code>
        </p>
        <p><code>+=</code>
        </p>
        <p><code>-=</code>
        </p>
        <p><code>*=</code>
        </p>
        <p><code>/=</code>
        </p>
        <p><code>%=</code>
        </p>
        <p><code>|=</code>
        </p>
        <p><code>&amp;=</code>
        </p>
        <p><code>^=</code>
        </p>
        <p><code>&lt;&lt;=</code>
        </p>
        <p><code>&gt;&gt;=</code>
        </p>
      </td>
      <td style="text-align:left">右至左</td>
    </tr>
    <tr>
      <td style="text-align:left">17</td>
      <td style="text-align:left"><code>throw</code> (擲回運算式)</td>
      <td style="text-align:left">右至左</td>
    </tr>
    <tr>
      <td style="text-align:left">18</td>
      <td style="text-align:left"><code>,</code> (逗號)</td>
      <td style="text-align:left">左至右</td>
    </tr>
  </tbody>
</table>