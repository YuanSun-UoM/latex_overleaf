# Processing  Journal Articles

## Files in overleaf 在overleaf中管理各类文件

### Directory 目录

- 期刊论文从开始准备到最终发表是一个漫长的过程，妥善管理文件非常必要。

#### 0_template 文件夹

- Upload Latex template files from the targeted journal website; 从期刊官网下载latex模板，上传在0_template文件夹中，方便后续查阅；

#### 1_draft 文件夹

- Upload Latex template files from the targeted journal website; 从期刊官网下载latex模板，上传在1_draft文件夹中，初稿直接在模板上写；
- Create a 'graphics' sub-folder for figures; 图片保存在1_draft/graphics 文件夹中
- Rename the main Latex file, such as 'paper_UrbanAlbedo_JAMES.tex'; 重命名
  - 'paper_' + keyword + journal name + '.tex''; 
- Link your Overleaf with your Zotero and add a bibliography file: 将Overleaf和Zotero关联，并且添加bib文件；
  - 'ref' + keyword + journal name + 'bib'

![add_bib](./add_bib.jpg)

### 2_manuscript 文件夹

- This section is done by the corresponding author; 通讯作者提交文件
- This folder is for the submitted version of your manuscript to journal, including .tex, .bib, .cls files;
- Create a 'submission_files' sub-folder; 

### 2_preprint 文件夹

- This folder is for the submitted version of your manuscript to preprint website, including .tex, .bib, .cls files; 准备preprint版本的文件（preprint版本可能会在manuscript版本上修改一些地方，例如隐去期刊信息）

### 3_reviews_1 文件夹

- This folder is for the first-round review; 
- Upload reviewers' comments by screenshot, markdown, or pdf files;
- Use '\todo{XXX}' to highlight the modified words 'XXX'; 通过\todo{}高亮修改的部分，从而与原始版本区分开来

### 3_revised_paper_1 文件夹

- Copy your '1_draft' folder and renamed as '3_revised_paper_1' for revision;
- Rename the main Latex file such as 'revised_UrbanAlbedo_JAMES.tex'
- Upload '[response_to_review](./response_to_review/)' template as a sub-folder; 
- After all authors agree, copy the main Latex file and rename such as'cleaned_revised_UrbanAlbedo_JAMES.tex'; 干净的版本删掉多余的工具包，以免期刊系统无法识别
  - Avoid using extra packages that the template tex does not have;
  - delete '\todo{}';



## Submission Tips 交稿阶段注意事项

### Figure

- Most figures are drawn in Python. Keep the code well for open research; 保留好Python画图的代码

- All figures should be in pdf format;

  

### Open Research

- Contribute to group GitHub following the samples: [NC_paper](https://github.com/zhonghua-zheng/code_uhws), [DynamicAlbedo](https://github.com/envdes/code_DynamicUrbanAlbedo);
- Each project would have a seperate repository for all files;



## Revision Tips 修稿阶段注意事项

- Do not modify anywhere that reviewer did not mention. 不要改审稿人没有提到的地方，只改审稿人要求改的地方，避免画蛇添足；



# AGU Journal Requirement

## Open Research

- For each citable data and software source (e.g., DOI, URL) you have mentioned in your Open Research section, please create a Reference List entry that describes and links to the resource. Please include a bracketed description of the data or software object, for example [Dataset] or [Software], in the Reference List entries. For more information about how to cite your data and software in your References List, please see [https://www.agu.org/Publish-with-AGU/Publish/Author-Resources/Data-and-Software-for-Authors#citation [agu.org\]](https://urldefense.com/v3/__https://www.agu.org/Publish-with-AGU/Publish/Author-Resources/Data-and-Software-for-Authors*citation__;Iw!!PDiH4ENfjr2_Jw!F_rPt3e5_9QjrCaEjB9KjMyPuKdLKy8PMHZ4RKxch6PPB_yGhDjdcx9bUVdrQ49CKen90tCLM9HzcJDLkZR9F5NG$)


**For example, please add the following citation to your References List:

Zhonghua Zheng, & Yuan Sun. (2024). envdes/code_DynamicUrbanAlbedo: First release by envdes (v0.0.1) [Software]. Zenodo.[https://doi.org/10.5281/ZENODO.10903399](https://urldefense.com/v3/__https://doi.org/10.5281/ZENODO.10903399__;!!PDiH4ENfjr2_Jw!F_rPt3e5_9QjrCaEjB9KjMyPuKdLKy8PMHZ4RKxch6PPB_yGhDjdcx9bUVdrQ49CKen90tCLM9HzcJDLkWlY0ywy$)

- For any original data, or data with accompanying citations, please use the (Name, Year) format of the citation in the Open Research section instead of the full link.
