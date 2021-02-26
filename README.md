# Esp32SynchronizationContext

It's rough to debug IoT devices. Many do not have integrated debugger probes and even the ones that do run over a slow interface like serial UART or at best, JTAG. This means step through debugging is either off the table or so slow as to be more painful than useful.

It's even worse to debug multithreaded code. Safely accessing data between threads is not for the faint of heart, and any wrong move can result in intermittent problems which are extremely difficult to track down, even on a full PC with an integrated debugging environment.

Forget about combining the two, especially given the ESP32's serial interface leading to long development and debug cycles. It's just not economical. Either that or you'll go nuts.

As a consequence, you've probably been running your fancy dual core ESP32 on a single core, leaving the other one to rot. You don't have to. What if I told you we could dramatically simplify general case synchronization, so you can freely create multithreaded code without all the fuss?

Read more: https://www.codeproject.com/Articles/5295781/Use-Both-Cores-on-an-ESP32-Easy-Synchronization-wi
