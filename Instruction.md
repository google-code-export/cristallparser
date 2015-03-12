# Instruction #

Available for unstable version.<br>
<h2>1. First Step</h2>
<h3>1.1 Download actual version</h3>
Stable (0.1) -> <a href='http://code.google.com/p/cristallparser/source/browse/?name=stable'>Source Code</a> <br>
Unstable (0.2) -> <a href='http://code.google.com/p/cristallparser/source/browse/?name=unstable'>Source Code</a>
<h3>1.2. Check Depends</h3>

CristallParser require libs/package:<br>
<br>
<table><thead><th>cmake</th><th>2.6</th></thead><tbody>
<tr><td>make</td><td>3.8</td></tr>
<tr><td>gcc</td><td>4.6</td></tr></tbody></table>

You download need libs and got next step<br>
<br>
<h3>3. Compile and install lib</h3>
In project dir open terminal/cmd and enter<br>
<pre><code> cmake .<br>
 make<br>
</code></pre>
next install libCristallParser.so to /usr/local/lib<br>
<br>
<h2>2. Documentation</h2>

<br>

<h3>void CristallParser::addGrammar</h3>
<pre><code>(<br>
 string Label, - #Your Label Name Rule<br>
 string Char   - #Char when define rule<br>
)<br>
</code></pre>

<h3>void CristallParser::addGrammarTo</h3>
<pre><code>(<br>
 string Label,  - #Your Label Name Rule<br>
 string StartChar, - # Begin char<br>
 string EndChar,     # Char what define end rule<br>
 int RunRuleInside   - { <br>
                          CristallRunGrammarInside, #Allow Parse other rules in this rule<br>
                          CristallRunNoGrammarInside #disallow Parse other rules in this rule<br>
                       }<br>
                        <br>
)<br>
</code></pre>
<h3>void CristallParser::addRule</h3>
<pre><code>(<br>
 string YourName, #Your name rule<br>
 int Rule,        - {<br>
                      CristallRuleWord         #Detect alphabet char<br>
                      CristallRuleNumbers      #Detect digits<br>
                    }<br>
 int Limit        - { CristallNoLimit or Numbers } #define limit chars/numbers to detect <br>
)<br>
</code></pre>

<h3>map < int, map < const char, string > > CristallParser::run()</h3>
Run parsing rules and returrn stucture:<br>
<pre><code>map [ int ] [ { 'Label',  ] = string; <br>
                'Value' }<br>
<br>
</code></pre>
<h3>void setData</h3>
<pre><code>(<br>
string Data              #Get data from variable Data to Parse<br>
)<br>
</code></pre>