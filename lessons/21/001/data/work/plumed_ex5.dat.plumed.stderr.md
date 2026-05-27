Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():

(core/GenericMolInfo.cpp:324) void PLMD::GenericMolInfo::interpretSymbol(const std::string&, std::vector<PLMD::AtomNumber>&)
Error importing MDAnalysis module: No module named 'MDAnalysis'
[runnervmg397c:79936] *** Process received signal ***
[runnervmg397c:79936] Signal: Aborted (6)
[runnervmg397c:79936] Signal code:  (-6)
[runnervmg397c:79936] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe1fe245330]
[runnervmg397c:79936] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe1fe29eb2c]
[runnervmg397c:79936] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe1fe24527e]
[runnervmg397c:79936] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe1fe2288ff]
[runnervmg397c:79936] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe1fe6a5ff5]
[runnervmg397c:79936] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe1fe6bb0da]
[runnervmg397c:79936] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe1fe6a5a55]
[runnervmg397c:79936] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe1fe6a5a6f]
[runnervmg397c:79936] [ 8] plumed(+0x13209)[0x560b23278209]
[runnervmg397c:79936] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe1fe22a1ca]
[runnervmg397c:79936] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe1fe22a28b]
[runnervmg397c:79936] [11] plumed(+0x134a5)[0x560b232784a5]
[runnervmg397c:79936] *** End of error message ***
</pre>
{% endraw %}
