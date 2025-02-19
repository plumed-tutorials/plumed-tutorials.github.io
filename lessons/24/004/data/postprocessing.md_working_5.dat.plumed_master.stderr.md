Stderr for source:  postprocessing.md_working_5.dat   
Download: [zipped raw stdout](postprocessing.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @18 : keyword ARG is compulsory for this action
[fv-az1690-151:06597] *** Process received signal ***
[fv-az1690-151:06597] Signal: Aborted (6)
[fv-az1690-151:06597] Signal code:  (-6)
[fv-az1690-151:06597] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efead445330]
[fv-az1690-151:06597] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efead49eb2c]
[fv-az1690-151:06597] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efead44527e]
[fv-az1690-151:06597] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efead4288ff]
[fv-az1690-151:06597] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efead8a5ff5]
[fv-az1690-151:06597] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efead8bb0da]
[fv-az1690-151:06597] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efead8a5a55]
[fv-az1690-151:06597] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efead8a5a6f]
[fv-az1690-151:06597] [ 8] plumed_master(+0x146dd)[0x562b6e3366dd]
[fv-az1690-151:06597] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efead42a1ca]
[fv-az1690-151:06597] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efead42a28b]
[fv-az1690-151:06597] [11] plumed_master(+0x15365)[0x562b6e337365]
[fv-az1690-151:06597] *** End of error message ***
</pre>
{% endraw %}
