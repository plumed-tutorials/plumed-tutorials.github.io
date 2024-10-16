Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[fv-az1426-552:06662] *** Process received signal ***
[fv-az1426-552:06662] Signal: Aborted (6)
[fv-az1426-552:06662] Signal code:  (-6)
[fv-az1426-552:06662] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1912242520]
[fv-az1426-552:06662] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f19122969fc]
[fv-az1426-552:06662] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1912242476]
[fv-az1426-552:06662] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f19122287f3]
[fv-az1426-552:06662] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f19126a2b9e]
[fv-az1426-552:06662] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f19126ae20c]
[fv-az1426-552:06662] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f19126ae277]
[fv-az1426-552:06662] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f19126ae52b]
[fv-az1426-552:06662] [ 8] plumed(+0x12f48)[0x562f907f4f48]
[fv-az1426-552:06662] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1912229d90]
[fv-az1426-552:06662] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1912229e40]
[fv-az1426-552:06662] [11] plumed(+0x131e5)[0x562f907f51e5]
[fv-az1426-552:06662] *** End of error message ***
</pre>
{% endraw %}
