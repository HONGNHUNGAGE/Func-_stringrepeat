Local $sresult
	Select
		Case NOT StringIsInt($irepeatcount)
			SetError(1)
			Return ""
		Case StringLen($sstring) < 1
			SetError(1)
			Return ""
		Case $irepeatcount <= 0
			SetError(1)
			Return ""
		Case Else
			For $icount = 1 To $irepeatcount
				$sresult &= $sstring
			Next
			Return $sresult
	EndSelect
EndFunc
