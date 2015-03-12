Micro Parser with simple rules:

Stable (0.2) -> [Source Code](http://code.google.com/p/cristallparser/source/browse/?name=stable) <br>
Unstable (0.3) -> <a href='http://code.google.com/p/cristallparser/source/browse/?name=unstable'>Source Code</a> <br>
Check Documentation -> <a href='http://code.google.com/p/cristallparser/wiki/Instruction'>Instruction</a> <a href='OutDated.md'>OutDated</a>
Example Use:<br>
<br>
<pre><code>
#include &lt;iostream&gt;
#include "CristallParser.h"
using namespace std;
using namespace Cristall
int main()
{
    CristallValues Val;
    CristallParser D;
    D.addRule("numbers", Rules::Numbers, (int)Limits::None);
    D.addRule("word", Rules::Letters, (int)Limits::None);
    D.setData("    Test word number 2555   ");
    Val = D.run();
    for(int i =0; i&lt;Val.size(); i++)
    {
        cout&lt;&lt;Vals.getElement(i, DataType::Label)&lt;&lt;" "&lt;&lt;Vals.getElement(i, DataType::Value)&lt;&lt;endl;
    }
    return 0;
}
</code></pre>