# JBL
Uibot

//猫窝纪主任标题
Dim arrayData,objExcelWorkBook,arrayRet
objExcelWorkBook=Excel.BindBook("测试.xlsx")
arrayData=UiElement.DataScrap({"wnd":[{"cls":"Chrome_WidgetWin_1","title":"*","app":"chrome"},{"cls":"Chrome_RenderWidgetHostHWND","title":"Chrome Legacy Window"}],"html":[{"tag":"TABLE","id":"threadlisttableid"}]},{"ExtractTable":0,"Columns":[{"selecors":[{"tag":"tbody","value":"tbody","index":0,"prefix":""},{"tag":"tr","index":0,"className":"","value":"tr","prefix":">"},{"tag":"th","index":0,"className":"common","value":"th.common","prefix":">"},{"tag":"a","index":0,"className":"s xstt","value":"a.s.xstt","prefix":">"}],"props":["text","url"]}]},{"objNextLinkElement":{"wnd":[{"cls":"Chrome_WidgetWin_1","title":"*","app":"chrome"},{"cls":"Chrome_RenderWidgetHostHWND","title":"Chrome Legacy Window"}],"html":[{"tag":"A","parentid":"fd_page_bottom","aaname":"下一页"}]},"iMaxNumberOfPage":13,"iMaxNumberOfResult":-1,"iDelayBetweenMS":1000,"bContinueOnError":False})
TracePrint($PrevResult)
Excel.WriteCell(objExcelWorkBook,"Sheet1","A1",arrayData,true)
