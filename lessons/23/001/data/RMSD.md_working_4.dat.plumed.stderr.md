Stderr for source:  RMSD.md_working_4.dat   
Download: [zipped raw stdout](RMSD.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:103) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[fv-az1426-552:06518] *** Process received signal ***
[fv-az1426-552:06518] Signal: Aborted (6)
[fv-az1426-552:06518] Signal code:  (-6)
[fv-az1426-552:06518] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fa48ce42520]
[fv-az1426-552:06518] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fa48ce969fc]
[fv-az1426-552:06518] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fa48ce42476]
[fv-az1426-552:06518] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fa48ce287f3]
[fv-az1426-552:06518] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fa48d2a2b9e]
[fv-az1426-552:06518] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fa48d2ae20c]
[fv-az1426-552:06518] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fa48d2ae277]
[fv-az1426-552:06518] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fa48d2ae52b]
[fv-az1426-552:06518] [ 8] plumed(+0x12f48)[0x55c000358f48]
[fv-az1426-552:06518] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fa48ce29d90]
[fv-az1426-552:06518] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fa48ce29e40]
[fv-az1426-552:06518] [11] plumed(+0x131e5)[0x55c0003591e5]
[fv-az1426-552:06518] *** End of error message ***
</pre>
{% endraw %}
