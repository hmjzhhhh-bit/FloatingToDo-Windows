# Floating To-Do — Windows trial

A private trial build of the Windows floating task list.

`FloatingToDo-Windows-Source.zip` contains the complete Tauri/Rust/HTML source project, dependency lockfiles, tests, build script and documentation. It preserves the complete folder structure when uploaded through GitHub’s web interface.

The Windows Actions workflow extracts the source, runs tests and generates an NSIS installer. Download **FloatingToDo-Windows-x64** from the successful run’s Artifacts, unzip it and share the `*-setup.exe` with your tester.

Requires Windows 10/11 x64. The installer can download Microsoft WebView2 if needed. This trial is unsigned. Native window behavior and the installation must still be tested on Windows.

For local development, extract the source ZIP and read its README.md. No personal tasks are included.
