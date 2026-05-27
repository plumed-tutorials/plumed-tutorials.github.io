Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervmg397c:79958] *** Process received signal ***
[runnervmg397c:79958] Signal: Aborted (6)
[runnervmg397c:79958] Signal code:  (-6)
[runnervmg397c:79958] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f24da445330]
[runnervmg397c:79958] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f24da49eb2c]
[runnervmg397c:79958] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f24da44527e]
[runnervmg397c:79958] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f24da4288ff]
[runnervmg397c:79958] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f24da8a5ff5]
[runnervmg397c:79958] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f24da8bb0da]
[runnervmg397c:79958] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f24da8a5a55]
[runnervmg397c:79958] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f24da8a5a6f]
[runnervmg397c:79958] [ 8] plumed_master(+0x146dd)[0x5567be1506dd]
[runnervmg397c:79958] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f24da42a1ca]
[runnervmg397c:79958] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f24da42a28b]
[runnervmg397c:79958] [11] plumed_master(+0x15365)[0x5567be151365]
[runnervmg397c:79958] *** End of error message ***
</pre>
{% endraw %}
