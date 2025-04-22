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
[fv-az1279-640:07125] *** Process received signal ***
[fv-az1279-640:07125] Signal: Aborted (6)
[fv-az1279-640:07125] Signal code:  (-6)
[fv-az1279-640:07125] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7febc1445330]
[fv-az1279-640:07125] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7febc149eb2c]
[fv-az1279-640:07125] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7febc144527e]
[fv-az1279-640:07125] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7febc14288ff]
[fv-az1279-640:07125] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7febc18a5ff5]
[fv-az1279-640:07125] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7febc18bb0da]
[fv-az1279-640:07125] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7febc18a5a55]
[fv-az1279-640:07125] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7febc18a5a6f]
[fv-az1279-640:07125] [ 8] plumed_master(+0x146dd)[0x55abb0f3f6dd]
[fv-az1279-640:07125] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7febc142a1ca]
[fv-az1279-640:07125] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7febc142a28b]
[fv-az1279-640:07125] [11] plumed_master(+0x15365)[0x55abb0f40365]
[fv-az1279-640:07125] *** End of error message ***
</pre>
{% endraw %}
