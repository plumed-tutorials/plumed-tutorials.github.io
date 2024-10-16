Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[fv-az573-691:04352] *** Process received signal ***
[fv-az573-691:04352] Signal: Aborted (6)
[fv-az573-691:04352] Signal code:  (-6)
[fv-az573-691:04352] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa74d042520]
[fv-az573-691:04352] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa74d0969fc]
[fv-az573-691:04352] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa74d042476]
[fv-az573-691:04352] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa74d0287f3]
[fv-az573-691:04352] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa74d4a2b9e]
[fv-az573-691:04352] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa74d4ae20c]
[fv-az573-691:04352] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa74d4ae277]
[fv-az573-691:04352] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa74d4ae52b]
[fv-az573-691:04352] [ 8] plumed(+0x12f48)[0x555bf4b06f48]
[fv-az573-691:04352] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa74d029d90]
[fv-az573-691:04352] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa74d029e40]
[fv-az573-691:04352] [11] plumed(+0x131e5)[0x555bf4b071e5]
[fv-az573-691:04352] *** End of error message ***
</pre>
{% endraw %}
