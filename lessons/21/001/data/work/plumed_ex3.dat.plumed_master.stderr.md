Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervmg397c:79883] *** Process received signal ***
[runnervmg397c:79883] Signal: Aborted (6)
[runnervmg397c:79883] Signal code:  (-6)
[runnervmg397c:79883] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd4bd645330]
[runnervmg397c:79883] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd4bd69eb2c]
[runnervmg397c:79883] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd4bd64527e]
[runnervmg397c:79883] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd4bd6288ff]
[runnervmg397c:79883] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd4bdaa5ff5]
[runnervmg397c:79883] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd4bdabb0da]
[runnervmg397c:79883] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd4bdaa5a55]
[runnervmg397c:79883] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd4bdaa5a6f]
[runnervmg397c:79883] [ 8] plumed_master(+0x146dd)[0x55feab4606dd]
[runnervmg397c:79883] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd4bd62a1ca]
[runnervmg397c:79883] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd4bd62a28b]
[runnervmg397c:79883] [11] plumed_master(+0x15365)[0x55feab461365]
[runnervmg397c:79883] *** End of error message ***
</pre>
{% endraw %}
