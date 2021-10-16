#include <GuiConstantsEx.au3>

#include <WindowsConstants.au3>
#Include <ScreenCapture.au3>
#Include <Misc.au3>
#include "ImageSearch2015.au3"

HotKeySet("{F1}", "_change")
HotKeySet("{F11}", "_quit")


;~ $GUI = GUICreate("d2", 240, 50)
;~ GUISetState()

Local $ss_hp = (@ScriptDir & "\ss\ss_hp.bmp")
Local $ss_portal = (@ScriptDir & "\ss\ss_portal.bmp")
Local $ss_start = (@ScriptDir & "\ss\ss_start.bmp")
Local $ss_malah = (@ScriptDir & "\ss\ss_malah.bmp")
Local $ss_error = (@ScriptDir & "\ss\ss_error.bmp")
Local $ss_host = (@ScriptDir & "\ss\ss_host.bmp")
Local $ss_perfgem = (@ScriptDir & "\ss\ss_perfgem.bmp")
Local $ss_perfgem2 = (@ScriptDir & "\ss\ss_perfgem2.bmp")
Local $ss_charm = (@ScriptDir & "\ss\ss_charm.bmp")
Local $picture1 = (@ScriptDir & "\ss\1.bmp"), $picture2 = (@ScriptDir & "\ss\2.bmp"), $picture3 = (@ScriptDir & "\ss\3.bmp")
Local $returnX = 0, $returnY = 0
Local $HK_count = 102
Local $diablo2 = "Diablo II: Resurrected"
$hp_pot = 1
While 1
	Switch GUIGetMsg()
		Case $GUI_EVENT_CLOSE
			Exit
	EndSwitch

WEnd

Func _change()
	Local $diablo2 = "Diablo II: Resurrected"
	If WinExists($diablo2) = False Then _relog()
	Sleep(2000)
	Local $returnX = 0, $returnY = 0
	$HK_host = _ImageSearchArea($ss_host, 1, 859, 625, 1004, 695, $returnX, $returnY, 0, 0)
	if $HK_host = True then
		Sleep(1000)
		MouseClick("left", 1270, 76)
		Sleep(500)
		MouseClick("left", 1321, 172)
		Sleep(500)
		Send("vers" & $HK_count)
		Sleep(500)
		Send("{TAB}")
		Sleep(500)
		Send("asdf")
		Sleep(500)
		Send("{ENTER}")
		$HK_count = $HK_count +1
		Sleep(1000)
	EndIf

	Local $returnX = 0, $returnY = 0
	$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
	if $HK_start = False then
		$begin1 = TimerInit ()
		While 1
			Local $returnX = 0, $returnY = 0
			$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
			if $HK_start = True then ExitLoop
			$dif = TimerDiff ($begin1)
			if $dif > 80000 then ExitLoop
			Sleep(100)
		WEnd
	EndIf

	Sleep(1000)
	Local $returnX = 0, $returnY = 0
	$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
	if $HK_start = True then
		Local $returnX = 0, $returnY = 0
		$HK_hp = _ImageSearchArea($ss_hp, 1,500, 932, 519, 952, $returnX, $returnY, 22, 0)
		If $HK_hp = False Then Send($hp_pot)
		$hp_pot = $hp_pot + 1
		If $hp_pot > 4 Then $hp_pot = 1


		MouseClick("left",648, 884,1,1)
		Sleep(1300)
		MouseClick("left",672, 696,1,5)
		Sleep(1200)
		MouseClick("left",1004, 880,1,5)
		Sleep(1300)
		MouseMove(1299, 458,5)
	EndIf

	$begin1 = TimerInit ()
	While 1
		Local $ss_stash = (@ScriptDir & "\ss\ss_stash.bmp")
		Local $returnX = 0, $returnY = 0
		$HK_stash = _ImageSearchArea($ss_stash, 1, 1089, 296, 1550, 650, $returnX, $returnY, 30, 0)
		If $HK_stash = True then
			MouseClick("left",$returnX, $returnY + 100,1, 5)
			ExitLoop
		Else
			Sleep(10)
		EndIf

		$dif = TimerDiff ($begin1)
		If $dif > 4000 then
			Send("{ESC}")
			sleep(100)
			MouseClick("left",956, 481,1,5)
			sleep(100)
			ExitLoop
		EndIf
	WEnd













	Sleep(2000)
	Local $returnX = 0, $returnY = 0
	$ss_inventory = (@ScriptDir & "\ss\ss_inventory.bmp")
	$HK_inventory = _ImageSearchArea($ss_inventory, 1, 275, 33,392, 83, $returnX, $returnY, 0, 0)
	If $HK_inventory = True Then
		Local $returnX = 0, $returnY = 0
		$ss_nextinventory = (@ScriptDir & "\ss\ss_nextinventory.bmp")
		$HK_nextinventory = _ImageSearchArea($ss_nextinventory, 1, 51, 137,621, 707, $returnX, $returnY, 50, 0)
		If $HK_nextinventory = False 	Then MouseClick("left", 249, 117, 1, 1)


		Local $ss_stash[10]
		Local $HK_stash[10]
		Send("{CTRLDOWN}")
		$x = 1320
		For $i = 0 to 4 Step +1
			$ss_stash[$i] = (@ScriptDir & "\ss\ss_stash" & $i & ".bmp")
			$HK_stash[$i] = _ImageSearchArea($ss_stash[$i], 1, 1200, 470, 1708, 761, $returnX, $returnY, 0, 0)
				For $y = 560 To 740 Step +60
					$HK_stash[$i] = _ImageSearchArea($ss_stash[$i], 1, 1273, 504, 1708, 761, $returnX, $returnY, 0, 0)
					If $HK_stash[$i] = True Then ContinueLoop
					MouseClick("left", $x, $y, 1, 1)
					Sleep(250)
				Next
				$x = $x + 60
		Next
		Send("{CTRLUP}")
		Send("{SPACE}")
	EndIf




























	Sleep(1000)

	$begin2 = TimerInit ()
	While 1
		$dif = TimerDiff ($begin2)
		if $dif > 3200 then exitloop
		MouseClick("left", 254, 963)
		Sleep(20)
	WEnd

	Sleep(2300)

	Local $diablo2 = "Diablo II: Resurrected"
	Local $returnX = 0, $returnY = 0
	$begin3 = TimerInit ()
	While 1
		$dif = TimerDiff ($begin3)
		$HK_portal = _ImageSearchArea($ss_portal, 1, 460, 60, 900, 500, $returnX, $returnY, 20, 0)
		If $HK_portal = True Then
			MouseClick("left", $returnX, $returnY,1,5)
;~ 			ToolTip("1",0,0)
			Exitloop
		EndIf
		If $dif > 5000 Then ExitLoop
		If WinExists($diablo2) = False Then _relog()
		Sleep(100)

	WEnd

	Local $returnX = 0, $returnY = 0
	$begin4 = TimerInit ()
	While 1

		$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
		if $HK_start = True then ExitLoop
		$dif = TimerDiff ($begin4)
		if $dif > 8000 then ExitLoop
		Sleep(100)
	WEnd

	Local $returnX = 0, $returnY = 0
	$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
	if $HK_start = True then
		Sleep(5000)
		Send("{LALT}")
		sleep(350)
		Send("{F3}")
		sleep(700)
		MouseClick("right", 1483, 119)
		sleep(700)
		MouseClick("right", 1483, 119)
		sleep(700)
		MouseClick("right", 1683, 50)
		sleep(450)

		Send("{F4}")
		MouseClick("right", 1296, 329)
		sleep(350)
		Send("{F2}")
		MouseClick("right", 1254, 312)
		sleep(350)
		MouseClick("right", 1275, 326)
		sleep(350)
		MouseClick("right", 1274, 320)
		sleep(350)
		MouseClick("right", 1265, 318)
		sleep(350)


		Send("{F4}")
		MouseClick("right", 1376, 289)
		sleep(350)
		Send("{F2}")
		MouseClick("right", 1254, 312)
		sleep(350)
		MouseClick("right", 1275, 326)
		sleep(350)
		MouseClick("right", 1274, 320)
		sleep(350)
		MouseClick("right", 1265, 318)
		sleep(350)

		Send("{F4}")
		MouseClick("right", 1262, 353)
		sleep(350)
		Send("{F3}")
		MouseClick("right", 1262, 353)
		sleep(1750)
		Send("{F4}")
		MouseClick("right", 962, 507)
	EndIf
_ScreenCapture_Capture(@ScriptDir & "\sx\sx_" & $HK_count & "1.bmp")
	$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
	Local $ss_hp = (@ScriptDir & "\ss\ss_hp.bmp")
	$HK_hp = _ImageSearchArea($ss_hp, 1,500, 932, 519, 952, $returnX, $returnY, 22, 0)
	If $HK_hp = False And $HK_start = True Then Send($hp_pot)
		$hp_pot = $hp_pot + 1
		If $hp_pot > 4 Then $hp_pot = 1
	$begin5 = TimerInit ()

	While 1
		$dif = TimerDiff ($begin5)
		if $dif > 3000 then exitloop
		$HK_start = _ImageSearchArea($ss_start, 1, 327, 895, 375, 949, $returnX, $returnY, 0, 0)
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($picture1,1, 640, 238, 1903, 1018, $returnX, $returnY,0,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($picture2,1, 640, 238, 1903, 1018, $returnX, $returnY,0,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($picture3,1, 640, 238, 1903, 1018 , $returnX, $returnY,0,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($ss_perfgem,1, 640, 238, 1903, 1018 , $returnX, $returnY,20,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($ss_perfgem2,1, 640, 238, 1903, 1018 , $returnX, $returnY,20,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd
		Local $returnX = 0, $returnY = 0
		While _ImageSearchArea($ss_charm,1, 640, 238, 1903, 1018 , $returnX, $returnY,20,0) And $HK_start = True
			MouseClick("left",$returnX +5,$returnY +10,1,5)
		WEnd

	WEnd
	_ScreenCapture_Capture(@ScriptDir & "\sx\sx_" & $HK_count & "2.bmp")

	if $HK_start = True then
		Sleep(500)
		Send("{ESC}")
		sleep(100)
		MouseClick("left",956, 481)
		Sleep(100)
	EndIf

	_relog()

EndFunc

Func _relog()
	$d2activate = WinActive ("Diablo II: Resurrected")
	If $d2activate = False Then WinActivate("Diablo II: Resurrected")
	Local $diablo2 = "Diablo II: Resurrected"
	Local $ss_lobby = (@ScriptDir & "\ss\ss_lobby.bmp")
	Local $ss_error = (@ScriptDir & "\ss\ss_error.bmp")
	Local $ss_blizzard = (@ScriptDir & "\ss\ss_blizzard.bmp")
	Local $returnX = 0, $returnY = 0
	$HK_error = _ImageSearchArea($ss_error, 1, 400,190,1450,850, $returnX, $returnY, 0, 0)
	If $HK_error = True then ProcessClose("Diablo II: Resurrected")
	If $HK_error = True then ProcessClose("d2r")
	If $HK_error = True then ProcessClose("d2r.exe")
	Sleep(1000)
	If WinExists($diablo2) = True Then
		Sleep(10)
	Else
		Run("C:\Program Files (x86)\Diablo II Resurrected\D2R.exe")
		WinActivate("Diablo II: Resurrected")
		Sleep(6000)
		Send("{SPACE}")
		Sleep(3000)
		Send("{SPACE}")

		Local $returnX = 0, $returnY = 0
		Sleep(1000)
		Do
			$HK_blizzard = _ImageSearchArea($ss_blizzard, 1, 656, 676,1367, 1013, $returnX, $returnY, 0, 0)
			If $HK_blizzard =  True Then Send("{SPACE}")
			If $HK_blizzard =  True Then ExitLoop
			Sleep(100)
		Until $HK_blizzard = True

		Sleep(1000)
		Do
			$HK_lobby = _ImageSearchArea($ss_lobby, 1, 1000,800,1200,1100, $returnX, $returnY, 0, 0)
			If $HK_lobby =  True Then MouseClick("left",$returnX, $returnY,1, 10)
			If $HK_lobby =  True Then ExitLoop
			Sleep(100)
		Until $HK_lobby = True
		Sleep(1000)
	EndIf
	Sleep(10000)
	_change()
EndFunc

Func _quit()
	Exit
EndFunc   ;==>_quit

;~ 		Do
;~ 			$HK_lobby = _ImageSearchArea($ss_lobby, 1, 1000,800,1200,1100, $returnX, $returnY, 0, 0)
;~ 			Send("{SPACE}")
;~ 			Sleep(1000)
;~ 		Until $HK_lobby = False
;~ 		Sleep(2000)
;~ 		Send("{SPACE}")


