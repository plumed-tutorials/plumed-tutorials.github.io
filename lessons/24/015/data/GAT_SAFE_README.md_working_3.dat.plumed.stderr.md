Stderr for source:  GAT_SAFE_README.md_working_3.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cv1 ATOMS=@mdatoms IMPORT=pycvPersistentData CALCULATE=pydist INIT=pyinit
Maybe a missing space or a typo?
[fv-az1778-96:04418] *** Process received signal ***
[fv-az1778-96:04418] Signal: Aborted (6)
[fv-az1778-96:04418] Signal code:  (-6)
[fv-az1778-96:04418] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f2996242520]
[fv-az1778-96:04418] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f29962969fc]
[fv-az1778-96:04418] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f2996242476]
[fv-az1778-96:04418] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f29962287f3]
[fv-az1778-96:04418] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f29966a2b9e]
[fv-az1778-96:04418] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f29966ae20c]
[fv-az1778-96:04418] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f29966ae277]
[fv-az1778-96:04418] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f29966ae52b]
[fv-az1778-96:04418] [ 8] plumed(+0x12f48)[0x557543c65f48]
[fv-az1778-96:04418] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f2996229d90]
[fv-az1778-96:04418] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f2996229e40]
[fv-az1778-96:04418] [11] plumed(+0x131e5)[0x557543c661e5]
[fv-az1778-96:04418] *** End of error message ***
</pre>
{% endraw %}
