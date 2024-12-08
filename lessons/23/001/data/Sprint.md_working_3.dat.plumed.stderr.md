Stderr for source:  Sprint.md_working_3.dat   
Download: [zipped raw stdout](Sprint.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action SPRINT with label ss : keyword MATRIX is compulsory for this action
[fv-az1020-777:04804] *** Process received signal ***
[fv-az1020-777:04804] Signal: Aborted (6)
[fv-az1020-777:04804] Signal code:  (-6)
[fv-az1020-777:04804] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff81b642520]
[fv-az1020-777:04804] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff81b6969fc]
[fv-az1020-777:04804] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff81b642476]
[fv-az1020-777:04804] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff81b6287f3]
[fv-az1020-777:04804] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff81baa2b9e]
[fv-az1020-777:04804] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff81baae20c]
[fv-az1020-777:04804] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff81baae277]
[fv-az1020-777:04804] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff81baae52b]
[fv-az1020-777:04804] [ 8] plumed(+0x12f48)[0x559a15654f48]
[fv-az1020-777:04804] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff81b629d90]
[fv-az1020-777:04804] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff81b629e40]
[fv-az1020-777:04804] [11] plumed(+0x131e5)[0x559a156551e5]
[fv-az1020-777:04804] *** End of error message ***
</pre>
{% endraw %}
