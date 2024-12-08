Stderr for source:  RMSD.md_working_3.dat   
Download: [zipped raw stdout](RMSD.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:103) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[fv-az1020-777:06404] *** Process received signal ***
[fv-az1020-777:06404] Signal: Aborted (6)
[fv-az1020-777:06404] Signal code:  (-6)
[fv-az1020-777:06404] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe8f9a42520]
[fv-az1020-777:06404] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe8f9a969fc]
[fv-az1020-777:06404] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe8f9a42476]
[fv-az1020-777:06404] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe8f9a287f3]
[fv-az1020-777:06404] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe8f9ea2b9e]
[fv-az1020-777:06404] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe8f9eae20c]
[fv-az1020-777:06404] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe8f9eae277]
[fv-az1020-777:06404] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe8f9eae52b]
[fv-az1020-777:06404] [ 8] plumed(+0x12f48)[0x55fe480aef48]
[fv-az1020-777:06404] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe8f9a29d90]
[fv-az1020-777:06404] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe8f9a29e40]
[fv-az1020-777:06404] [11] plumed(+0x131e5)[0x55fe480af1e5]
[fv-az1020-777:06404] *** End of error message ***
</pre>
{% endraw %}
