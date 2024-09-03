
It's simply an interface to Google Storage that looks like a file system. Calls to the filesystem are converted to Google Storage API requests, I believe. It won't download data in a file until you request that specific file - definitely doesn't attempt to download the whole mounted share at the start.

The one big issue is that it doesn't show directories created outside of GCSFuse interactions, which can be confusing if you 'ls' a directory with a bunch of sub-directories and don't see anything.

Technically if you upload a file to some subdirectory with gsutil, the parent directories don't exist in a certain sense. That's why you don't see them.

What does GCSFuse do?

GCSFuse — also known as Google Cloud Storage FUSE — is an open-source Fuse adapter for mounting and accessing cloud storage buckets (using Google Cloud Storage) as local file systems. It lets you read and write objects in your bucket using standard file system semantics.