Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @67 : keyword ARG is compulsory for this action
[fv-az1755-505:06424] *** Process received signal ***
[fv-az1755-505:06424] Signal: Aborted (6)
[fv-az1755-505:06424] Signal code:  (-6)
[fv-az1755-505:06424] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1adfa45330]
[fv-az1755-505:06424] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1adfa9eb2c]
[fv-az1755-505:06424] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1adfa4527e]
[fv-az1755-505:06424] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1adfa288ff]
[fv-az1755-505:06424] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1adfea5ff5]
[fv-az1755-505:06424] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1adfebb0da]
[fv-az1755-505:06424] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1adfea5a55]
[fv-az1755-505:06424] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1adfea5a6f]
[fv-az1755-505:06424] [ 8] plumed_master(+0x146dd)[0x5609854c56dd]
[fv-az1755-505:06424] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1adfa2a1ca]
[fv-az1755-505:06424] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1adfa2a28b]
[fv-az1755-505:06424] [11] plumed_master(+0x15365)[0x5609854c6365]
[fv-az1755-505:06424] *** End of error message ***
</pre>
{% endraw %}
