Stderr for source:  Behler.md_working_5.dat   
Download: [zipped raw stdout](Behler.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1020-777:05364] *** Process received signal ***
[fv-az1020-777:05364] Signal: Aborted (6)
[fv-az1020-777:05364] Signal code:  (-6)
[fv-az1020-777:05364] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd790242520]
[fv-az1020-777:05364] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd7902969fc]
[fv-az1020-777:05364] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd790242476]
[fv-az1020-777:05364] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd7902287f3]
[fv-az1020-777:05364] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd7906a2b9e]
[fv-az1020-777:05364] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd7906ae20c]
[fv-az1020-777:05364] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd7906ae277]
[fv-az1020-777:05364] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd7906ae52b]
[fv-az1020-777:05364] [ 8] plumed(+0x12f48)[0x56155293ef48]
[fv-az1020-777:05364] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd790229d90]
[fv-az1020-777:05364] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd790229e40]
[fv-az1020-777:05364] [11] plumed(+0x131e5)[0x56155293f1e5]
[fv-az1020-777:05364] *** End of error message ***
</pre>
{% endraw %}
