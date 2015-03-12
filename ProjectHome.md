Micro Parser with simple rules:

Stable (0.2) -> [Source Code](http://code.google.com/p/cristallparser/source/browse/?name=stable) <br>
Unstable (0.3) -> <a href='http://code.google.com/p/cristallparser/source/browse/?name=unstable'>Source Code</a> <br>
Check Documentation -> <a href='http://code.google.com/p/cristallparser/wiki/Instruction'>Instruction</a> <a href='OutDated.md'>OutDated</a>
Example Use:<br>
<br>
<pre><code><br>
#include &lt;iostream&gt;<br>
#include "CristallParser.h"<br>
using namespace std;<br>
using namespace Cristall<br>
int main()<br>
{<br>
    CristallValues Val;<br>
    CristallParser D;<br>
    D.addRule("numbers", Rules::Numbers, (int)Limits::None);<br>
    D.addRule("word", Rules::Letters, (int)Limits::None);<br>
    D.setData("    Test word number 2555   ");<br>
    Val = D.run();<br>
    for(int i =0; i&lt;Val.size(); i++)<br>
    {<br>
        cout&lt;&lt;Vals.getElement(i, DataType::Label)&lt;&lt;" "&lt;&lt;Vals.getElement(i, DataType::Value)&lt;&lt;endl;<br>
    }<br>
    return 0;<br>
}<br>
</code></pre>