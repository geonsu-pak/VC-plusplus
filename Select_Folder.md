## CFolderPickerDialog
<pre>
CFolderPickerDialog folderPickerDialog(
                                       _T("D:\\work\\"), 
                                       OFN_FILEMUSTEXIST | OFN_ALLOWMULTISELECT | OFN_ENABLESIZING, 
                                       this, 
                                       sizeof(OPENFILENAME));
CString folderPath;
if (folderPickerDialog.DoModal() == IDOK) {
		POSITION pos = folderPickerDialog.GetStartPosition();
		while (pos) {
			folderPath = folderPickerDialog.GetNextPathName(pos);
		}
}
</pre>
