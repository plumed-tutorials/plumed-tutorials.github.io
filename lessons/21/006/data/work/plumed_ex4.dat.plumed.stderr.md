Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DUMPPDB ATOMS=cc_data ATOM_INDICES=@nonhydrogens FILE=traj.pdb
Maybe a missing space or a typo?
[fv-az1778-96:05920] *** Process received signal ***
[fv-az1778-96:05920] Signal: Aborted (6)
[fv-az1778-96:05920] Signal code:  (-6)
[fv-az1778-96:05920] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fbaec842520]
[fv-az1778-96:05920] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fbaec8969fc]
[fv-az1778-96:05920] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fbaec842476]
[fv-az1778-96:05920] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fbaec8287f3]
[fv-az1778-96:05920] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fbaecca2b9e]
[fv-az1778-96:05920] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fbaeccae20c]
[fv-az1778-96:05920] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fbaeccae277]
[fv-az1778-96:05920] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fbaeccae52b]
[fv-az1778-96:05920] [ 8] plumed(+0x12f48)[0x556c3a442f48]
[fv-az1778-96:05920] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fbaec829d90]
[fv-az1778-96:05920] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fbaec829e40]
[fv-az1778-96:05920] [11] plumed(+0x131e5)[0x556c3a4431e5]
[fv-az1778-96:05920] *** End of error message ***
</pre>
{% endraw %}
