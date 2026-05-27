Stderr for source:  Behler.md_working_6.dat   
Download: [zipped raw stdout](Behler.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervmg397c:80382] *** Process received signal ***
[runnervmg397c:80382] Signal: Aborted (6)
[runnervmg397c:80382] Signal code:  (-6)
[runnervmg397c:80382] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc9be045330]
[runnervmg397c:80382] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc9be09eb2c]
[runnervmg397c:80382] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc9be04527e]
[runnervmg397c:80382] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc9be0288ff]
[runnervmg397c:80382] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc9be4a5ff5]
[runnervmg397c:80382] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc9be4bb0da]
[runnervmg397c:80382] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc9be4a5a55]
[runnervmg397c:80382] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc9be4a5a6f]
[runnervmg397c:80382] [ 8] plumed(+0x13209)[0x558abf816209]
[runnervmg397c:80382] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc9be02a1ca]
[runnervmg397c:80382] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc9be02a28b]
[runnervmg397c:80382] [11] plumed(+0x134a5)[0x558abf8164a5]
[runnervmg397c:80382] *** End of error message ***
</pre>
{% endraw %}
