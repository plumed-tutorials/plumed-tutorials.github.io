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
[fv-az1279-640:07103] *** Process received signal ***
[fv-az1279-640:07103] Signal: Aborted (6)
[fv-az1279-640:07103] Signal code:  (-6)
[fv-az1279-640:07103] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3cb3845330]
[fv-az1279-640:07103] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3cb389eb2c]
[fv-az1279-640:07103] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3cb384527e]
[fv-az1279-640:07103] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3cb38288ff]
[fv-az1279-640:07103] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3cb3ca5ff5]
[fv-az1279-640:07103] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3cb3cbb0da]
[fv-az1279-640:07103] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3cb3ca5a55]
[fv-az1279-640:07103] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3cb3ca5a6f]
[fv-az1279-640:07103] [ 8] plumed(+0x13209)[0x55b04e374209]
[fv-az1279-640:07103] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3cb382a1ca]
[fv-az1279-640:07103] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3cb382a28b]
[fv-az1279-640:07103] [11] plumed(+0x134a5)[0x55b04e3744a5]
[fv-az1279-640:07103] *** End of error message ***
</pre>
{% endraw %}
