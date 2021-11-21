# StringSplit
#include &lt;Array.au3> ; for testing Global $sDirectory = @WindowsDir, $sStdOut  $PID = Run(@ComSpec &amp; ' /c DIR "' &amp; $sDirectory &amp; '" /B /A-D /O-D', "", @SW_HIDE, 2) ; /O-D = newest first, 2 = $STDOUT_CHILD While Not @error     $sStdOut &amp;= StdoutRead($PID) WEnd $aStdOut = StringSplit(StringStripWS($sStdOut, 7), @CRLF) _ArrayDisplay($aStdOut) ; for testing
