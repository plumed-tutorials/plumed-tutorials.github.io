Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PCA with label pca : action cc has no component named cc (hint! the components in this actions are: )
[fv-az1690-151:06440] *** Process received signal ***
[fv-az1690-151:06440] Signal: Aborted (6)
[fv-az1690-151:06440] Signal code:  (-6)
[fv-az1690-151:06440] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5dc7045330]
[fv-az1690-151:06440] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5dc709eb2c]
[fv-az1690-151:06440] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5dc704527e]
[fv-az1690-151:06440] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5dc70288ff]
[fv-az1690-151:06440] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5dc74a5ff5]
[fv-az1690-151:06440] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5dc74bb0da]
[fv-az1690-151:06440] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5dc74a5a55]
[fv-az1690-151:06440] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5dc74a5a6f]
[fv-az1690-151:06440] [ 8] plumed(+0x13209)[0x561b7c3c8209]
[fv-az1690-151:06440] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5dc702a1ca]
[fv-az1690-151:06440] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5dc702a28b]
[fv-az1690-151:06440] [11] plumed(+0x134a5)[0x561b7c3c84a5]
[fv-az1690-151:06440] *** End of error message ***
</pre>
{% endraw %}
