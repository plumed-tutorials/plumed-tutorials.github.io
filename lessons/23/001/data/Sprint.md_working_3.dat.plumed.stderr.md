Stderr for source:  Sprint.md_working_3.dat   
Download: [zipped raw stdout](Sprint.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label ss : keyword MATRIX is compulsory for this action
[runnervmg397c:79486] *** Process received signal ***
[runnervmg397c:79486] Signal: Aborted (6)
[runnervmg397c:79486] Signal code:  (-6)
[runnervmg397c:79486] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fef0a845330]
[runnervmg397c:79486] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fef0a89eb2c]
[runnervmg397c:79486] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fef0a84527e]
[runnervmg397c:79486] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fef0a8288ff]
[runnervmg397c:79486] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fef0aca5ff5]
[runnervmg397c:79486] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fef0acbb0da]
[runnervmg397c:79486] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fef0aca5a55]
[runnervmg397c:79486] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fef0aca5a6f]
[runnervmg397c:79486] [ 8] plumed(+0x13209)[0x55a51eede209]
[runnervmg397c:79486] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fef0a82a1ca]
[runnervmg397c:79486] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fef0a82a28b]
[runnervmg397c:79486] [11] plumed(+0x134a5)[0x55a51eede4a5]
[runnervmg397c:79486] *** End of error message ***
</pre>
{% endraw %}
