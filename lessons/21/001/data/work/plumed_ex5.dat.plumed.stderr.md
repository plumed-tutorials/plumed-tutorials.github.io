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
[fv-az1279-640:07180] *** Process received signal ***
[fv-az1279-640:07180] Signal: Aborted (6)
[fv-az1279-640:07180] Signal code:  (-6)
[fv-az1279-640:07180] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f38acc45330]
[fv-az1279-640:07180] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f38acc9eb2c]
[fv-az1279-640:07180] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f38acc4527e]
[fv-az1279-640:07180] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f38acc288ff]
[fv-az1279-640:07180] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f38ad0a5ff5]
[fv-az1279-640:07180] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f38ad0bb0da]
[fv-az1279-640:07180] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f38ad0a5a55]
[fv-az1279-640:07180] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f38ad0a5a6f]
[fv-az1279-640:07180] [ 8] plumed(+0x13209)[0x5613cba5e209]
[fv-az1279-640:07180] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f38acc2a1ca]
[fv-az1279-640:07180] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f38acc2a28b]
[fv-az1279-640:07180] [11] plumed(+0x134a5)[0x5613cba5e4a5]
[fv-az1279-640:07180] *** End of error message ***
</pre>
{% endraw %}
