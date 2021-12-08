## Select File
<pre>
const TCHAR szFilter[] = _T("BMP Files (*.bmp)|*.dat|All Files (*.*)|*.*||");
CFileDialog dlg(TRUE, _T("dat"), NULL, OFN_HIDEREADONLY | OFN_OVERWRITEPROMPT, szFilter, this);
if (dlg.DoModal() == IDOK) {
		CString sFilePath = dlg.GetPathName();
		c_lut.SetWindowText(sFilePath);
}
</pre>
