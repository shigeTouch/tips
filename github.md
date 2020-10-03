 Command + Shift + P  
 Markdown: Open Preview to the Side  
 .md ファイルを開いている状態で、「Command + K」を押してから、  
 一度手を離して、「V」を押すと  

 ## バージョン確認  
 ``` $ git --version```  

 ## 設定確認  
 ### ローカル  
 ``` $ git config -l ```  
 ### グローバル  
 ``` $v git config --global -l ```  
 
 ※ -l = --list  

## 設定内容  
### 1. git ユーザー名、メールアドレスの設定  
 ``` $ git config --global user.name "John Doe" ```  
 ``` $ git config --global user.email johndoe@example.com ```  

### 2. ディレクトリ、ファイル設定   

中身が空のフォルダを作成  
 ``` $ mkdir ~/.ssh ```  

中身が空のファイルを作成   
 ``` $ touch ~/.ssh/config ```  

所有者のみ読み込み権限  
 ``` $ chmod 700 ~/.ssh ```  

所有者のみ読み込み／書き込み権限  
 ``` $ chmod 600 ~/.ssh/* ```  

MACのファイル属性（パーミッション）に付与される「@」を一括削除  
 ``` $ xattr -cr ~/.ssh ```  

### 3. sshファイル編集  

``` $ vi ~/.ssh/config``` 

``` Host * ```  
```   StrictHostKeyChecking no```  
```   UserKnownHostsFile=/dev/null```   
```   ServerAliveInterval 15```   
```   ServerAliveCountMax 30```  
```   AddKeysToAgent yes```  
```   UseKeychain yes```  
```   IdentitiesOnly yes```  

### ローカルにgit clone作成
``` git clone https://github.com/^^^^^/リポジトリ名.git ```

[引用：公式サイト](https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA-Git-%E3%81%AE%E8%A8%AD%E5%AE%9A)  
[引用：Qiita Mac Git初期設定](https://qiita.com/ucan-lab/items/aadbedcacbc2ac86a2b3#ssh-config)







