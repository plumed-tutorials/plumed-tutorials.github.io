Stderr for source:  ./solutions/walker-0/plumed_reweight_newcv.dat   
Download: [zipped raw stdout](plumed_reweight_newcv.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight_newcv.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1755-505:05459] *** Process received signal ***
[fv-az1755-505:05459] Signal: Aborted (6)
[fv-az1755-505:05459] Signal code:  (-6)
[fv-az1755-505:05459] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1397845330]
[fv-az1755-505:05459] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f139789eb2c]
[fv-az1755-505:05459] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f139784527e]
[fv-az1755-505:05459] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f13978288ff]
[fv-az1755-505:05459] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1397ca5ff5]
[fv-az1755-505:05459] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1397cbb0da]
[fv-az1755-505:05459] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1397ca5a55]
[fv-az1755-505:05459] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1397ca5a6f]
[fv-az1755-505:05459] [ 8] plumed_master(+0x146dd)[0x5612866a76dd]
[fv-az1755-505:05459] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f139782a1ca]
[fv-az1755-505:05459] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f139782a28b]
[fv-az1755-505:05459] [11] plumed_master(+0x15365)[0x5612866a8365]
[fv-az1755-505:05459] *** End of error message ***
</pre>
{% endraw %}
