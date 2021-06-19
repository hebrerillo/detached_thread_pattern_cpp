# detached_thread_pattern_cpp

Example code that represents a situation where a detached thread is more convenient than a thread that should be joined.

A use case would be an application that has to download a file on demand in the background.

The user commands the application to download the file, and the application creates a detached thread to start the download process. Once the download process is done, the detached thread terminates.

The alternative would be to create a joinable thread that would receive notifications from the main thread to download a file. The main drawback of this approach is that the thread is created and destroyed along with the main application, thus consuming CPU time. That is, the thread has the same life spawn as the main application.

