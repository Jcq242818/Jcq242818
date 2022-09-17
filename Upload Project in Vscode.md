### We all know that git is a Version Control System (VCS) to better manage our code, project files. Vscode allows you to upload code or project files to a Github remote repository using Git. Here are a few key points for uploading.

- 首先，Github是远程代码仓库，而我们本地也存在一个代码仓库。git要做的事情就是将我们需要上传的代码放到缓存区，之后通过commit将需要上传的代码移交到本地的代码仓库，最后才可以由本地的代码仓库将相关代码上传到github。

- 下图即为代码已经成功存储在本地的代码仓库后的界面：

![image-20220917235704318](https://user-images.githubusercontent.com/113497191/190867087-eeba9c59-258c-4cc2-b190-eb13a5e23fdd.png)

- 之后，我们要点击这个**发布Branch**，即可在github上创建一个远程仓库，注意，这个时候也会在本地创建一个名字叫**origin**远程仓库，这个仓库和GitHub上我们新命名的仓库是相互绑定的关系。即假如我们删除了Github上新命名的仓库，那么我们就无法在本地将代码上传到Github上，会显示找不到Github上对应的仓库。（因为我们发布Branch的时候就创建了本地origin远程仓库和Github上自己命名的仓库，Github上的仓库删去后由于本地origin仓库还和其相绑定，因此我们无法在本地继续向Github上传代码）如下图所示：

![image-20220918000937268](https://user-images.githubusercontent.com/113497191/190867124-a0428959-5665-4474-be12-1a2e30cfb08f.png)

- 如果删去了GitHub上对应的仓库，本地还想对修改过后的代码进行同步更改上传到Github上的话，只能删去本地**origin**远程仓库，使其与该代码工程解除绑定关系，如下所示：

![image-20220918001151050](https://user-images.githubusercontent.com/113497191/190867132-90b19585-4dc1-46b6-ba1a-4dc9c18da7d6.png)

                                                             图.删除本地的远程库origin

- 删除了本地的远程库后，该代码工程就恢复到了移交到本地的代码仓库后准备生成本地和Github上的两个绑定的远程仓库上传到Github上的过程，我们重复上面的步骤即可重新发布一个新的Branch。

![image-20220918001338564](https://user-images.githubusercontent.com/113497191/190867143-84a4783d-1b3f-48c5-bd56-e1f53dc09bc0.png)

- 特别注意的是，本地的远程库origin受代码工程绑定，不同的工程有不同的本地远程库，但是他们的命名都是origin，且互不影响。只要是移交到本地的代码仓库的工程文件，用Vscode打开后都可以直接显示到如下界面：

![image-20220918002152560](https://user-images.githubusercontent.com/113497191/190867186-774d0919-8436-4118-8d84-e10ced07dfaf.png)

- 最后，再次总结一下，本地的远程库origin和Github上我们命名的新仓库是相互绑定的，当我们删除了Github上的新仓库后，除非把本地的远程库origin也删除了，不然无法上传该代码工程后续的修改的版本。
