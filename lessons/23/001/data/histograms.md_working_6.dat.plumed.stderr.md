Stderr for source:  histograms.md_working_6.dat   
Download: [zipped raw stdout](histograms.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: RDF LABEL=rdf GROUP=1-1000 GRID_BIN=100 MAXR=1.0 BANDWIDTH=0.01
Maybe a missing space or a typo?
[fv-az1426-552:06176] *** Process received signal ***
[fv-az1426-552:06176] Signal: Aborted (6)
[fv-az1426-552:06176] Signal code:  (-6)
[fv-az1426-552:06176] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6cdee42520]
[fv-az1426-552:06176] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6cdee969fc]
[fv-az1426-552:06176] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6cdee42476]
[fv-az1426-552:06176] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6cdee287f3]
[fv-az1426-552:06176] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6cdf2a2b9e]
[fv-az1426-552:06176] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6cdf2ae20c]
[fv-az1426-552:06176] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6cdf2ae277]
[fv-az1426-552:06176] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6cdf2ae52b]
[fv-az1426-552:06176] [ 8] plumed(+0x12f48)[0x5563a3785f48]
[fv-az1426-552:06176] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6cdee29d90]
[fv-az1426-552:06176] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6cdee29e40]
[fv-az1426-552:06176] [11] plumed(+0x131e5)[0x5563a37861e5]
[fv-az1426-552:06176] *** End of error message ***
</pre>
{% endraw %}
