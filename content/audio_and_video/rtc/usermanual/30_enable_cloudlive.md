---
title: "云录制管理"
draft: false
collapsible: false
weight: 30
---

录制需要进行音视频流的转码或转封装，会产生服务器计算资源的消耗，因此需要按照录制业务对计算资源的占用成本进行收费。

云端录制功能默认关闭，启用云端录制功能需要先开通对象存储功能。录播内容存储将按照对象存储收费。

## 前提条件

已开启对象存储。

## 操作步骤

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **音视频** > **实时音视频 RTC**，进入实时音视频 RTC 的**概览**页面。

   ![](../../_images/qs_app_list.png)

3. 在左侧导航栏中，点击**应用管理**，进入应用管理页面。

   ![](../../_images/um_app_list.png)

4. 点击需要编辑的应用的名称，进入应用详情页面。

5. 在开启云录制配置所在行，点击 <img src="../../_images/icon_closed.png" style="zoom:75%;" />。

   ![](../../_images/um_edit_cloudlive.png)

   参数说明，如下表所示。

   <table class="table table-bordered table-striped table-condensed">
     <tr>
       <td>
         参数
       </td>
       <td>
         参数说明
       </td>
     </tr>
       <tr>
       <td>
         分辨率
       </td>
       <td>
         录制音视频的分辨率。分辨率会影响音视频的清晰度，分辨率低图像比较模糊，分辨率高图像更清晰。
       </td>
     </tr>
     <tr>
       <td>
         音频格式
       </td>
       <td>
         录制的音频文件的格式，可以保存为音频文件：aac格式。
       </td>
     </tr>
       <tr>
       <td>
         视频格式
       </td>
       <td>
         录制的视频文件的格式，可以保存为：mp4格式。
       </td>
     </tr>
         <tr>
       <td>
         文件存储位置
       </td>
       <td>
         存储位置为青云的对象存储服务。请先开启对象存储服务，并创建桶，详细请参见《对象存储服务用户指南》。<br />为了不影响您已有的对象存储业务，请创建新的桶。<br />录播文件的前缀为<i>CloudRecordMedia/</i>。
       </td>
     </tr>
         <tr>
       <td>
         录制布局
       </td>
       <td>
         当前青云提供的录制布局，包含<b>悬浮布局</b>、<b>自适应布局</b>和<b>垂直布局</b>。请根据您实际情况进行选择。
       </td>
     </tr>
   </table>

6. 配置完成后，点击**提交**。

   您可以在云录制列表中，查看已配置的云录播信息。包含云录制开启状态、录制码率、文件存储位置、文件保存时长以及选择录制布局。
