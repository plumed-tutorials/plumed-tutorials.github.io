Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[pkrvmf6wy0o8zjz:61331] *** Process received signal ***
[pkrvmf6wy0o8zjz:61331] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61331] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61331] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faa49045330]
[pkrvmf6wy0o8zjz:61331] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faa4909eb2c]
[pkrvmf6wy0o8zjz:61331] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faa4904527e]
[pkrvmf6wy0o8zjz:61331] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faa490288ff]
[pkrvmf6wy0o8zjz:61331] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faa494a5ff5]
[pkrvmf6wy0o8zjz:61331] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faa494bb0da]
[pkrvmf6wy0o8zjz:61331] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faa494a5a55]
[pkrvmf6wy0o8zjz:61331] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faa494a5a6f]
[pkrvmf6wy0o8zjz:61331] [ 8] plumed(+0x13209)[0x5644db6eb209]
[pkrvmf6wy0o8zjz:61331] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faa4902a1ca]
[pkrvmf6wy0o8zjz:61331] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faa4902a28b]
[pkrvmf6wy0o8zjz:61331] [11] plumed(+0x134a5)[0x5644db6eb4a5]
[pkrvmf6wy0o8zjz:61331] *** End of error message ***
</pre>
{% endraw %}
