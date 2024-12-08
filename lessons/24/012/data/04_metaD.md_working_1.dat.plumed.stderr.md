Stderr for source:  04_metaD.md_working_1.dat   
Download: [zipped raw stdout](04_metaD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](04_metaD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: [TORSION](HTTPS://WWW.PLUMED.ORG/DOC-MASTER/USER-DOC/HTML/_T_O_R_S_I_O_N.HTML) LABEL=t1 ATOMS=1,6,4,5
Maybe a missing space or a typo?
[fv-az1778-96:04597] *** Process received signal ***
[fv-az1778-96:04597] Signal: Aborted (6)
[fv-az1778-96:04597] Signal code:  (-6)
[fv-az1778-96:04597] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f208fa42520]
[fv-az1778-96:04597] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f208fa969fc]
[fv-az1778-96:04597] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f208fa42476]
[fv-az1778-96:04597] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f208fa287f3]
[fv-az1778-96:04597] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f208fea2b9e]
[fv-az1778-96:04597] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f208feae20c]
[fv-az1778-96:04597] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f208feae277]
[fv-az1778-96:04597] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f208feae52b]
[fv-az1778-96:04597] [ 8] plumed(+0x12f48)[0x556fe6dc9f48]
[fv-az1778-96:04597] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f208fa29d90]
[fv-az1778-96:04597] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f208fa29e40]
[fv-az1778-96:04597] [11] plumed(+0x131e5)[0x556fe6dca1e5]
[fv-az1778-96:04597] *** End of error message ***
</pre>
{% endraw %}
