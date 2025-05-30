Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmf6wy0o8zjz:60000] *** Process received signal ***
[pkrvmf6wy0o8zjz:60000] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60000] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60000] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe1c0045330]
[pkrvmf6wy0o8zjz:60000] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe1c009eb2c]
[pkrvmf6wy0o8zjz:60000] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe1c004527e]
[pkrvmf6wy0o8zjz:60000] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe1c00288ff]
[pkrvmf6wy0o8zjz:60000] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe1c04a5ff5]
[pkrvmf6wy0o8zjz:60000] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe1c04bb0da]
[pkrvmf6wy0o8zjz:60000] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe1c04a5a55]
[pkrvmf6wy0o8zjz:60000] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe1c04a5a6f]
[pkrvmf6wy0o8zjz:60000] [ 8] plumed(+0x13209)[0x5610e9be1209]
[pkrvmf6wy0o8zjz:60000] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe1c002a1ca]
[pkrvmf6wy0o8zjz:60000] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe1c002a28b]
[pkrvmf6wy0o8zjz:60000] [11] plumed(+0x134a5)[0x5610e9be14a5]
[pkrvmf6wy0o8zjz:60000] *** End of error message ***
</pre>
{% endraw %}
