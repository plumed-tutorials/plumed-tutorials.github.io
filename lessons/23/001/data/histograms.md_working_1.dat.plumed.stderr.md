Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[fv-az1315-757:07799] *** Process received signal ***
[fv-az1315-757:07799] Signal: Aborted (6)
[fv-az1315-757:07799] Signal code:  (-6)
[fv-az1315-757:07799] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7f5ac45330]
[fv-az1315-757:07799] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7f5ac9eb2c]
[fv-az1315-757:07799] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7f5ac4527e]
[fv-az1315-757:07799] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7f5ac288ff]
[fv-az1315-757:07799] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7f5b0a5ff5]
[fv-az1315-757:07799] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7f5b0bb0da]
[fv-az1315-757:07799] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7f5b0a5a55]
[fv-az1315-757:07799] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7f5b0a5a6f]
[fv-az1315-757:07799] [ 8] plumed(+0x13209)[0x55c407c85209]
[fv-az1315-757:07799] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7f5ac2a1ca]
[fv-az1315-757:07799] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7f5ac2a28b]
[fv-az1315-757:07799] [11] plumed(+0x134a5)[0x55c407c854a5]
[fv-az1315-757:07799] *** End of error message ***
</pre>
{% endraw %}
