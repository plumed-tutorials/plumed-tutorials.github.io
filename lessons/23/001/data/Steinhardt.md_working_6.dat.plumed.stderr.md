Stderr for source:  Steinhardt.md_working_6.dat   
Download: [zipped raw stdout](Steinhardt.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmf6wy0o8zjz:59563] *** Process received signal ***
[pkrvmf6wy0o8zjz:59563] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59563] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59563] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa242845330]
[pkrvmf6wy0o8zjz:59563] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa24289eb2c]
[pkrvmf6wy0o8zjz:59563] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa24284527e]
[pkrvmf6wy0o8zjz:59563] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa2428288ff]
[pkrvmf6wy0o8zjz:59563] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa242ca5ff5]
[pkrvmf6wy0o8zjz:59563] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa242cbb0da]
[pkrvmf6wy0o8zjz:59563] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa242ca5a55]
[pkrvmf6wy0o8zjz:59563] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa242ca5a6f]
[pkrvmf6wy0o8zjz:59563] [ 8] plumed(+0x13209)[0x560e4034c209]
[pkrvmf6wy0o8zjz:59563] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa24282a1ca]
[pkrvmf6wy0o8zjz:59563] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa24282a28b]
[pkrvmf6wy0o8zjz:59563] [11] plumed(+0x134a5)[0x560e4034c4a5]
[pkrvmf6wy0o8zjz:59563] *** End of error message ***
</pre>
{% endraw %}
