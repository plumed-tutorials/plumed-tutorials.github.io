Stderr for source:  PIV-PathCV_meta.md_working_4.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GMX grompp -f md.mdp -c Liq.pdb -p TIP4P.top -o meta.tpr
Maybe a missing space or a typo?
[fv-az1778-96:04211] *** Process received signal ***
[fv-az1778-96:04211] Signal: Aborted (6)
[fv-az1778-96:04211] Signal code:  (-6)
[fv-az1778-96:04211] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f12c2842520]
[fv-az1778-96:04211] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f12c28969fc]
[fv-az1778-96:04211] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f12c2842476]
[fv-az1778-96:04211] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f12c28287f3]
[fv-az1778-96:04211] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f12c2ca2b9e]
[fv-az1778-96:04211] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f12c2cae20c]
[fv-az1778-96:04211] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f12c2cae277]
[fv-az1778-96:04211] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f12c2cae52b]
[fv-az1778-96:04211] [ 8] plumed(+0x12f48)[0x560ba02ccf48]
[fv-az1778-96:04211] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f12c2829d90]
[fv-az1778-96:04211] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f12c2829e40]
[fv-az1778-96:04211] [11] plumed(+0x131e5)[0x560ba02cd1e5]
[fv-az1778-96:04211] *** End of error message ***
</pre>
{% endraw %}
