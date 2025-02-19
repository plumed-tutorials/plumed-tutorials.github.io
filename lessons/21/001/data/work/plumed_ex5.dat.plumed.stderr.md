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
[fv-az1755-505:06591] *** Process received signal ***
[fv-az1755-505:06591] Signal: Aborted (6)
[fv-az1755-505:06591] Signal code:  (-6)
[fv-az1755-505:06591] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb484445330]
[fv-az1755-505:06591] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb48449eb2c]
[fv-az1755-505:06591] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb48444527e]
[fv-az1755-505:06591] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb4844288ff]
[fv-az1755-505:06591] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb4848a5ff5]
[fv-az1755-505:06591] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb4848bb0da]
[fv-az1755-505:06591] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb4848a5a55]
[fv-az1755-505:06591] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb4848a5a6f]
[fv-az1755-505:06591] [ 8] plumed(+0x13209)[0x55a6666ad209]
[fv-az1755-505:06591] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb48442a1ca]
[fv-az1755-505:06591] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb48442a28b]
[fv-az1755-505:06591] [11] plumed(+0x134a5)[0x55a6666ad4a5]
[fv-az1755-505:06591] *** End of error message ***
</pre>
{% endraw %}
