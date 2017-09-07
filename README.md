# GUI
# A very simple GUI using wxpython library

import wx

class  Frame1(wx.Frame):
    def __init__(self,superior):
        wx.Frame.__init__(self,parent =superior, title = 'Example', pos= (100,200), size = (350,200))
        self.panel = wx.Panel(self)
        self.panel.Bind(wx.EVT_LEFT_UP, self.OnClick)
        #text1 = wx.TextCtrl(panel, value = "Hello, World!", size = (350,200))

    def OnClick(self,event):
        posm = event.GetPosition()
        wx.StaticText(parent = self.panel, label= "Hello, World!", pos = (posm.x, posm.y))

if __name__ == "__main__":
    app = wx.App()
    frame = Frame1(None)
    frame.Show(True)
    app.MainLoop()
