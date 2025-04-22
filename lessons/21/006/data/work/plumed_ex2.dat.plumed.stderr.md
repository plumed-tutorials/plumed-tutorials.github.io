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
[fv-az2211-783:07208] *** Process received signal ***
[fv-az2211-783:07208] Signal: Aborted (6)
[fv-az2211-783:07208] Signal code:  (-6)
[fv-az2211-783:07208] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa2c8a45330]
[fv-az2211-783:07208] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa2c8a9eb2c]
[fv-az2211-783:07208] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa2c8a4527e]
[fv-az2211-783:07208] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa2c8a288ff]
[fv-az2211-783:07208] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa2c8ea5ff5]
[fv-az2211-783:07208] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa2c8ebb0da]
[fv-az2211-783:07208] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa2c8ea5a55]
[fv-az2211-783:07208] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa2c8ea5a6f]
[fv-az2211-783:07208] [ 8] plumed(+0x13209)[0x55ec02bd2209]
[fv-az2211-783:07208] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa2c8a2a1ca]
[fv-az2211-783:07208] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa2c8a2a28b]
[fv-az2211-783:07208] [11] plumed(+0x134a5)[0x55ec02bd24a5]
[fv-az2211-783:07208] *** End of error message ***
</pre>
{% endraw %}
