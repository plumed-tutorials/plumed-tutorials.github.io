Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervmg397c:79861] *** Process received signal ***
[runnervmg397c:79861] Signal: Aborted (6)
[runnervmg397c:79861] Signal code:  (-6)
[runnervmg397c:79861] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f70e2845330]
[runnervmg397c:79861] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f70e289eb2c]
[runnervmg397c:79861] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f70e284527e]
[runnervmg397c:79861] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f70e28288ff]
[runnervmg397c:79861] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f70e2ca5ff5]
[runnervmg397c:79861] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f70e2cbb0da]
[runnervmg397c:79861] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f70e2ca5a55]
[runnervmg397c:79861] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f70e2ca5a6f]
[runnervmg397c:79861] [ 8] plumed(+0x13209)[0x55c8f87a0209]
[runnervmg397c:79861] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f70e282a1ca]
[runnervmg397c:79861] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f70e282a28b]
[runnervmg397c:79861] [11] plumed(+0x134a5)[0x55c8f87a04a5]
[runnervmg397c:79861] *** End of error message ***
</pre>
{% endraw %}
