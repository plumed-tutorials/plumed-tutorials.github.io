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
[fv-az1755-505:06536] *** Process received signal ***
[fv-az1755-505:06536] Signal: Aborted (6)
[fv-az1755-505:06536] Signal code:  (-6)
[fv-az1755-505:06536] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0b71245330]
[fv-az1755-505:06536] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0b7129eb2c]
[fv-az1755-505:06536] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0b7124527e]
[fv-az1755-505:06536] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0b712288ff]
[fv-az1755-505:06536] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0b716a5ff5]
[fv-az1755-505:06536] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0b716bb0da]
[fv-az1755-505:06536] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0b716a5a55]
[fv-az1755-505:06536] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0b716a5a6f]
[fv-az1755-505:06536] [ 8] plumed_master(+0x146dd)[0x56208ec2f6dd]
[fv-az1755-505:06536] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0b7122a1ca]
[fv-az1755-505:06536] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0b7122a28b]
[fv-az1755-505:06536] [11] plumed_master(+0x15365)[0x56208ec30365]
[fv-az1755-505:06536] *** End of error message ***
</pre>
{% endraw %}
