# CNKI_Patent_SVM
文本分类是指在给定分类体系下 , 根据文本的内容自动确定文本类别的过程。首先我们根据scrapy爬虫根据中国知网URL的规律，爬取70多万条2014年公开的发明专利，然后通过数据清洗筛选出了60多万条含标签数据。通过TF-IDF对60多万条本文进行词频提取，依照词频排序提取前3000个词语形成语义词典，然后根据观察设置停用词。然后再用TF-IDF的方式对每个摘要进行词频选取，通过布尔模型，对比语义词典生成文本向量。然后对标签进行数字化转换。取90%的文本为训练集，10%的文本为测试集。用有监督学习的SVM算法对文本进行分类，（人类生活必需品、作业运输、化学冶金、纺织造纸、固定建筑物、机械工程、物理学、电学）分成8类
