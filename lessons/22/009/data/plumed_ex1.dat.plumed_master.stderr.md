Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[fv-az1690-151:06239] *** Process received signal ***
[fv-az1690-151:06239] Signal: Aborted (6)
[fv-az1690-151:06239] Signal code:  (-6)
[fv-az1690-151:06239] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6019045330]
[fv-az1690-151:06239] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f601909eb2c]
[fv-az1690-151:06239] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f601904527e]
[fv-az1690-151:06239] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f60190288ff]
[fv-az1690-151:06239] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f60194a5ff5]
[fv-az1690-151:06239] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f60194bb0da]
[fv-az1690-151:06239] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f60194a5a55]
[fv-az1690-151:06239] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f60194a5a6f]
[fv-az1690-151:06239] [ 8] plumed_master(+0x146dd)[0x5629852ac6dd]
[fv-az1690-151:06239] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f601902a1ca]
[fv-az1690-151:06239] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f601902a28b]
[fv-az1690-151:06239] [11] plumed_master(+0x15365)[0x5629852ad365]
[fv-az1690-151:06239] *** End of error message ***
</pre>
{% endraw %}
