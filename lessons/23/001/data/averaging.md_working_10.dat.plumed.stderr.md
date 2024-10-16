Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[fv-az1426-552:06033] *** Process received signal ***
[fv-az1426-552:06033] Signal: Aborted (6)
[fv-az1426-552:06033] Signal code:  (-6)
[fv-az1426-552:06033] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8952042520]
[fv-az1426-552:06033] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f89520969fc]
[fv-az1426-552:06033] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8952042476]
[fv-az1426-552:06033] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f89520287f3]
[fv-az1426-552:06033] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f89524a2b9e]
[fv-az1426-552:06033] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f89524ae20c]
[fv-az1426-552:06033] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f89524ae277]
[fv-az1426-552:06033] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f89524ae52b]
[fv-az1426-552:06033] [ 8] plumed(+0x12f48)[0x55768d938f48]
[fv-az1426-552:06033] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8952029d90]
[fv-az1426-552:06033] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8952029e40]
[fv-az1426-552:06033] [11] plumed(+0x131e5)[0x55768d9391e5]
[fv-az1426-552:06033] *** End of error message ***
</pre>
{% endraw %}
