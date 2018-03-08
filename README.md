# Mime-Detector

The mime detector for files (e.g. png, gif, jpeg, rtf, pdf, docx, zip, rar,...) helps to prevent attacker trying to upload or attack damage files to the web server.
Reference to [OWASP Top 10 - 2017](https://www.owasp.org/index.php/Top_10-2017_Top_10) for the risks.

> Based on https://github.com/Muraad/Mime-Detective

Usage 

```csharp

// Both ways are writing the data to a temp file
// to get a FileInfo. GetFileType are extension methods
byte[] fileData = ...;
FileType fileType = fileData.GetFileType();
   
// or 
Stream fileDataStream = ...;
FileType fileType = fileDataStream.GetFileType();

// If writing to a temp file is not practicable use it like this
byte[] fileData = ...;
FileType fileType = MimeTypes.GetFileType(() => fileData);
   
```

# Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :p

# Licence

Code released under [the MIT license](https://github.com/thangchung/Mime-Detector/blob/master/LICENSE).
