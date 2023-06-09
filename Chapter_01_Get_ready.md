# 準備開發環境 (Getting ready!)

[開發環境] 指的是撰寫各種程式時，需要先做好的設定以及軟體。以 Loki NLU 平台而言，我們通常會需要：

1. IDE (我強烈推薦 [Wing Pro](https://wingware.com/) ，以下的說明也將以 Wing Pro 擷圖示範說明。學校教育用途可申請 [Classroom Use](https://wingware.com/store/free) 的免費授權)
2. 終端機 (在 Mac/Linux 下，終端機又稱為 Terminal。在 Windows 下，則通常被稱做 [命令提示字元]。兩者開啟起來，都是一個黑黑 (或白白) 的視窗，用來輸入指令用的。

就這兩個東西，但因為 Windows 有各種不同的版本，而 Mac 又有兩種不同的 CPU 架構，在接下來的章節裡，我將提供各種不同的方案，請讀者依自己的電腦設備條件選擇其中一種

> - 我只知道是 Windows 的電腦，其它什麼都不知道 [傳送門](https://github.com/Droidtown/Loki_NLU_The_Handbook/blob/main/Chapter_01_Get_ready.md#%E5%8F%AA%E7%9F%A5%E9%81%93%E6%98%AF-windows-%E7%9A%84%E9%9B%BB%E8%85%A6%E5%85%B6%E5%AE%83%E4%BB%80%E9%BA%BC%E9%83%BD%E4%B8%8D%E7%9F%A5%E9%81%93)
> - 我的 VirtualBox 無法匯入 **NLP\_TrainingLab** 或無法運作 **NLP\_TrainingLab** [傳送門](https://github.com/Droidtown/Loki_NLU_The_Handbook/blob/main/Chapter_01_Get_ready.md#%E6%88%91%E7%9A%84-virtualbox-%E7%84%A1%E6%B3%95%E5%8C%AF%E5%85%A5-nlp_traininglab-%E6%88%96%E7%84%A1%E6%B3%95%E9%81%8B%E4%BD%9C-nlp_traininglab)
> - 我用 Mac 電腦。[傳送門](https://github.com/Droidtown/Loki_NLU_The_Handbook/blob/main/Chapter_01_Get_ready.md#%E6%88%91%E7%94%A8-mac-%E9%9B%BB%E8%85%A6-%E6%88%96-%E6%88%91%E7%94%A8-linux-%E9%9B%BB%E8%85%A6)
> - 我用 Linux 電腦。(同上)

----
## 只知道是 Windows 的電腦，其它什麼都不知道…
因為 Windows 的版本眾多，為了避免不同的 Winodws 各自的設定不同而雞同鴨講，所以我們準備了一個 VirtualBox 的虛擬機器，將設定全部做好了！

你可以簡單地把 VirtualBox 理解成「一部虛擬的電腦主機」，我們要在這部虛擬的電腦主機裡安裝一個虛擬的作業系統，叫做 NLP_TrainingLab。

 VirtualBox 虛擬機器是免費的，而 NLP_TrainingLab 虛擬系統也是免費的！

接下來有兩大部份，分別有三個步驟：
先下載與安裝 VirtualBox 虛擬主機

**1.1** 下載 VirtualBox：
先到這裡下載 VirtualBox：[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)  
![ ](./media/Chapter01_01.png  "Virtualbox_Download")
**1.2** 安裝 VirtualBox：
Windows 環境下的安裝，就依序完成 [下一步] 的指示即可。

**1.3** 啟動 VirtualBox 然後會看到類似以下的畫面：

#### 完成 VirtualBox 下載和安裝以後，接下來只要：

**2.1** 下載虛擬系統
點擊：下載連結
檔案有點大，約 3.5GB，請耐心稍待…

**2.2** 匯入虛擬系統  
	i. 啟動 VirtualBox  
		![ ](./media/Chapter01_02.png  "Virtualbox_Import_1")
	ii. 點擊左上方的 [工具] 接著點擊 [匯入]  
		![ ](./media/Chapter01_03.png  "Virtualbox_Import_2")

**2.3** 啟動虛擬系統
    啟動 VirtualBox  
		![ ](./media/Chapter01_04.png  "Virtualbox_Start_1")
    選擇虛擬系統 NLP_TrainingLab，再點擊 [啟動] 讓它開機，待出現以下畫面就完成開機囉  
		![ ](./media/Chapter01_05.png  "Virtualbox_Start_2")


----
## 我的 VirtualBox 無法匯入 NLP\_TrainingLab 或無法運作 NLP\_TrainingLab

如果無法安裝 VirtualBox，或無法匯入 NLP\_TrainingLab，又或是無法運作 NLP\_TrainingLab 的話，只要你的電腦裡沒有其它版本的 Python3，那麼就能依這段的說明設定好自己的系統。

接下來，首先[下載&安裝 PowerShell](https://github.com/PowerShell/PowerShell#get-powershell) 確認自己的電腦裡「**沒有**」Python3，接著[**下載&安裝 Python3**] 以及[**下載&安裝 Wing Pro**].

1. [下載&安裝 PowerShell](https://github.com/PowerShell/PowerShell#get-powershell)：打開連結以後，建議選擇 Windows (x64) 的 LTS 版本，下載以後完成安裝。
2. 確認自己的電腦裡沒有 Python3
	i. 從 [開始] 功能表，打開在前一步安裝的 PowerShell (按一下 [開始] 並輸入 PowerShell，然後點擊 [Windows PowerShell] 的圖示，啟動 PowerShell。  
		![ ](./media/Chapter01_06.png  "Start_PowerShell")  
	ii. 在 [PowerShell] 的游標處輸入 `where.exe python` 並按下 Enter，如果沒有找到 python 的話，接著做下一步，否則直接到步驟 3。  
	iii. 下載&安裝 Python3  
		![ ](./media/Chapter01_07.png  "Download_Python3")  
	下載完成以後，點擊剛才下載的檔案，開始安裝。特別注意在這個步驟時，要把 [Add python.exe to PATH] 勾起來！如果忘了勾，稍後可以解除安裝，再重來一次。  
		![ ](./media/Chapter01_08.png  "Install_Python3")
3. 下載&安裝 Wing Pro
    從 Wingware [下載 Wing Pro](https://wingware.com/) 並安裝到你的電腦裡。我個人十分推薦使用 Wing Pro，它是商業軟體，需要付費購買。但為學校教育使用的話，可以申請免費的授權碼。如果你不是學術單位，也可以使用 Wing Personal 的版本，基本功能幾乎一樣。  
		![ ](./media/Chapter01_11.png  "Wing")

這個步驟完成以後，你的電腦裡就有 PowerShell 和 Python3 了。
接下來，請在 PowerShell 的視窗裡，依序完成以下操作：

1. 輸入`python3 -m pip install requests` 按下 Enter 讓它完成
2. 輸入`python3 -m pip install discord.py` 按下 Enter 讓它完成
3. 輸入`python3 -m pip install ArticutAPI` 按下 Enter 讓它完成
4. 輸入`python3 -m pip install KeyMojiAPI` 按下 Enter 讓它完成

至此，你的 Windows 電腦已經準備好，可以進行 NLP 應用的開發工作了！


----
## 我用 Mac 電腦 或 我用 Linux 電腦。

Mac 或是 Linux 都已經內建預先裝好的 Python3，所以前述絕大多數的工作都不需要做。只要打開終端機 (Terminal) ，然後依序安裝幾個模組，然後再安裝 Wing Pro 就行了。

1. 打開終端機：  
    - Mac: 點擊 [啟動台] > 輸入 [Terminal] > 啟動 [Terminal]    
	![ ](./media/Chapter01_09.png  "Open_Terminal_1")
    - 在 Terminal 中依序輸入以下的內容，安裝 requests, discord.py, ArticutAPI 和 KeyMojiAPI 四個套件…    
	![ ](./media/Chapter01_10.png  "Open_Terminal_2")
	
    1. 輸入`python3 -m pip install requests` 按下 Enter 讓它完成
    2. 輸入`python3 -m pip install discord.py` 按下 Enter 讓它完成
    3. 輸入`python3 -m pip install ArticutAPI` 按下 Enter 讓它完成
    4. 輸入`python3 -m pip install KeyMojiAPI` 按下 Enter 讓它完成
2. 下載&安裝 Wing Pro
    從 Wingware [下載 Wing Pro](https://wingware.com/) 並安裝到你的電腦裡。我個人十分推薦使用 Wing Pro，它是商業軟體，需要付費購買。但為學校教育使用的話，可以申請免費的授權碼。如果你不是學術單位，也可以使用 Wing Personal 的版本，基本功能幾乎一樣。  
	![ ](./media/Chapter01_11.png  "Wing")

完成以後，你的電腦就已經準備好，可以進行 NLP 應用的開發工作了！