Stderr for source:  RMSD.md_working_2.dat   
Download: [zipped raw stdout](RMSD.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DISPLACEMENT LABEL=disp ARG1=d1,d2,d3 ARG2=d1_ref,d2_ref,d3_ref
Maybe a missing space or a typo?
[fv-az1426-552:06473] *** Process received signal ***
[fv-az1426-552:06473] Signal: Aborted (6)
[fv-az1426-552:06473] Signal code:  (-6)
[fv-az1426-552:06473] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc1d3a42520]
[fv-az1426-552:06473] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc1d3a969fc]
[fv-az1426-552:06473] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc1d3a42476]
[fv-az1426-552:06473] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc1d3a287f3]
[fv-az1426-552:06473] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc1d3ea2b9e]
[fv-az1426-552:06473] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc1d3eae20c]
[fv-az1426-552:06473] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc1d3eae277]
[fv-az1426-552:06473] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc1d3eae52b]
[fv-az1426-552:06473] [ 8] plumed(+0x12f48)[0x557ffc0c3f48]
[fv-az1426-552:06473] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc1d3a29d90]
[fv-az1426-552:06473] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc1d3a29e40]
[fv-az1426-552:06473] [11] plumed(+0x131e5)[0x557ffc0c41e5]
[fv-az1426-552:06473] *** End of error message ***
</pre>
{% endraw %}
