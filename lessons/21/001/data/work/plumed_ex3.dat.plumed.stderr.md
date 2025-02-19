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
[fv-az1755-505:06514] *** Process received signal ***
[fv-az1755-505:06514] Signal: Aborted (6)
[fv-az1755-505:06514] Signal code:  (-6)
[fv-az1755-505:06514] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3a51445330]
[fv-az1755-505:06514] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3a5149eb2c]
[fv-az1755-505:06514] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3a5144527e]
[fv-az1755-505:06514] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3a514288ff]
[fv-az1755-505:06514] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3a518a5ff5]
[fv-az1755-505:06514] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3a518bb0da]
[fv-az1755-505:06514] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3a518a5a55]
[fv-az1755-505:06514] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3a518a5a6f]
[fv-az1755-505:06514] [ 8] plumed(+0x13209)[0x56389853c209]
[fv-az1755-505:06514] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3a5142a1ca]
[fv-az1755-505:06514] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3a5142a28b]
[fv-az1755-505:06514] [11] plumed(+0x134a5)[0x56389853c4a5]
[fv-az1755-505:06514] *** End of error message ***
</pre>
{% endraw %}
