# Batch-download-from-Copernicus 
# Batch download of data from the Copernicus Data Center using OData (Sentinel 2, Sentinel 3, etc.)
# 哥白尼数据中心数据批量下载（如哨兵二号、三号等）
You need to change the first 7 lines of code according to your needs你需要根据自己的需求更改前8行代码

You can read it in English or Chinese, the content is the same 中英文含义一样，择一阅读。


Lines 1,2.Change the start and end time of the data you want to download 更改你想下载数据的起止时间

start_date = "2020-01-01"

end_date = "2020-12-31"

Line 3.Then the name of data collection. The currently supported data collection are shown in the figure ![a49b003b-cae0-4392-9450-0a0fa7b8841c](https://github.com/user-attachments/assets/cc8f4607-e54e-458d-95f2-936c6923c269)更改数据集名 支持的数据集如图所示

data_collection = "SENTINEL-3"

Line 4.As well as the coverage range.
  Please note that the download does not include cropping and mosaicking; it contains all the tiles within or partially within this range.
  At -10, change to the minimum longitude of the area you want; 4.0 ——>the maximum longitude; 35.5——>the minimum latitude; 44.0——>the maximum latitude

  更改区域范围。请注意并不包含裁剪和拼接，下载的数据会是所有含该区域或部分该区域的所有瓦片 -10部分替换为最小经度，4.0 ——>最大经度; 35.5——>最小纬度; 44.0——>最大纬度
  
aoi = "POLYGON((-10.0 44.0, -10.0 35.5, 4.0 35.5, 4.0 44.0, -10.0 44.0))"

Line 5.Go to this website: https://browser.dataspace.copernicus.eu/?zoom=5&lat=50.16282&lng=20.78613&themeId=DEFAULT-THEME&visualizationUrl=U2FsdGVkX18HNOrsb%2FWndmv%2BHz%2B0d8Hy22TUjoxyKSHcCP6kzyJd7SSRYlx4lK%2BjlSnXyfluh63C0ZMSN%2BqZmqEQ5Mwx84tIS%2Fe9f%2Fij1nxEqdAAxat7oXPygJcvr8VZ&datasetId=S2_L2A_CDAS&demSource3D=%22MAPZEN%22&cloudCoverage=30&dateMode=SINGLE
(using the Sentinel series data as an example; for other datasets, find the corresponding interface). Click SEARCH, select the dataset you want based on the product, and click Search at the bottom. Then randomly choose a file, click the i icon in the bottom right, expand Product, scroll down to find Product type, and paste it here. The operation diagram is as follows

进入上述网站（这里以Sentinel系列数据为例，其他数据集需要找到对应的界面），点击SEARCH，根据你想要的产品选好数据集，点击下方Search，随后随便找一个文件点击右下方i标志，展开Product，下滑找到Product type，粘贴到此处即可。操作图示如下方

product_type = "OL_2_LRR___"
![b19340d1-a844-43bf-b7b3-8bd3c7b3ab08](https://github.com/user-attachments/assets/64920af8-b033-4f8a-80ec-3aaebd0f17df)
![caa22d8e-874b-4097-961c-7e4ff3b198eb](https://github.com/user-attachments/assets/44b56d86-a1c2-4201-ab6e-12cf8b21c620)
![3ebf98ae-9baf-40f6-ae44-1e2d79325c16](https://github.com/user-attachments/assets/5a876689-4eed-40e7-89bc-a92714201958)
![b7f107f7-f328-46fe-b1ef-26698829c92e](https://github.com/user-attachments/assets/06c397d7-b19c-4a99-b670-8b737593fde8)

Lines 6, 7. Your username and password for the Copernicus Data Center 你在哥白尼数据中心的用户名和密码

username = "1111@1111.com"

password = "11111"

Line 8. Download Path 下载路径

download_dir = "D:/Yuxin/Data/S3_Ref"

