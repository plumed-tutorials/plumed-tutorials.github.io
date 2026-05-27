Stderr for source:  SymmetryFunction.md_working_3.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[runnervmg397c:80551] *** Process received signal ***
[runnervmg397c:80551] Signal: Aborted (6)
[runnervmg397c:80551] Signal code:  (-6)
[runnervmg397c:80551] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffb15645330]
[runnervmg397c:80551] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffb1569eb2c]
[runnervmg397c:80551] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffb1564527e]
[runnervmg397c:80551] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffb156288ff]
[runnervmg397c:80551] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffb15aa5ff5]
[runnervmg397c:80551] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffb15abb0da]
[runnervmg397c:80551] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffb15aa5a55]
[runnervmg397c:80551] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffb15aa5a6f]
[runnervmg397c:80551] [ 8] plumed(+0x13209)[0x55ebc42ce209]
[runnervmg397c:80551] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffb1562a1ca]
[runnervmg397c:80551] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffb1562a28b]
[runnervmg397c:80551] [11] plumed(+0x134a5)[0x55ebc42ce4a5]
[runnervmg397c:80551] *** End of error message ***
</pre>
{% endraw %}
