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
[fv-az1535-978:71647] *** Process received signal ***
[fv-az1535-978:71647] Signal: Aborted (6)
[fv-az1535-978:71647] Signal code:  (-6)
[fv-az1535-978:71647] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f38cb042520]
[fv-az1535-978:71647] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f38cb0969fc]
[fv-az1535-978:71647] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f38cb042476]
[fv-az1535-978:71647] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f38cb0287f3]
[fv-az1535-978:71647] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f38cb4a2b9e]
[fv-az1535-978:71647] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f38cb4ae20c]
[fv-az1535-978:71647] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f38cb4ae277]
[fv-az1535-978:71647] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f38cb4ae52b]
[fv-az1535-978:71647] [ 8] plumed(+0x12f48)[0x55d5ecfeef48]
[fv-az1535-978:71647] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f38cb029d90]
[fv-az1535-978:71647] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f38cb029e40]
[fv-az1535-978:71647] [11] plumed(+0x131e5)[0x55d5ecfef1e5]
[fv-az1535-978:71647] *** End of error message ***
</pre>
{% endraw %}
