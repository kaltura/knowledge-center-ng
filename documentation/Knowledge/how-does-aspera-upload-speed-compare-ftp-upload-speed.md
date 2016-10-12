---
layout: page
title: "How does the Aspera Upload Speed compare to the FTP Upload Speed?"
date: 2014-04-08 13:43:32
---

By default, Kaltura provides a 45mbps Aspera upload speed. The FTP comparison is dependent on your connection and latency and can only be measured by testing.

Aspera uses UDP which overcomes the inherent TCP congestion problem.

If you have a certain latency on your connection, you are likely to be slowed down by its duration. However, using TCP, you will pay for this latency every few packets. The upside is that TCP ensures the completeness of the transferred data as it is a statefull protocol.

With UDP, it's your (in this case Aspera's) responsibility to ensure the data integrity and to re-transmit whatever packets that were dropped along the way. However, you can keep throwing packets at maximum speed.

For more informaton see <a href="http://asperasoft.com/resources/benchmarks/#vsftp-630" target="_blank">FASP BENCHMARKS</a>.