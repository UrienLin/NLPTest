*****************************************************************************************
Please read NLPCC-ICCPOL-QA-2017.guideline.pdf for more details about tasks and datasets.
Thank you!
*****************************************************************************************

【NLPCC2017-OpenDomainQA评测工具包】主要由下面6部分组成：
	(1)code
		该文件夹包含针对KBQA任务、DBQA任务和TBQA任务搭建的三个基本baseline systems。
		在KBQA项目的Program.cs里面，能够找到针对KBQA任务的example code。
		在DBQA项目的Program.cs里面，能够找到针对DBQA任务的example code。
		在TBQA项目的Program.cs里面，能够找到针对TBQA任务的example code。
		请在64X环境下使用。
	(2)knowledge
		该文件夹内包含两个知识库文件：nlpcc-iccpol-2016.kbqa.kb和nlpcc-iccpol-2016.kbqa.kb.mention2id。
		nlpcc-iccpol-2016.kbqa.kb包含43M网络挖掘的知识库三元组，文件格式为：Subject ||| Predicate ||| Object
		nlpcc-iccpol-2016.kbqa.kb.mention2id是从nlpcc-iccpol-2016.kbqa.kb中抽取出来的文件，用于进行entity recognition，文件格式为：Entity Mention ||| Entity Name_1\t...\tEntity Name_N
		上述两个文件被KBQA系统调用。
	(3)model
		该文件夹包含三个子文件夹。
		template文件夹中包含问题模板样例文件，该文件被KBQA系统调用，用于语义分析[1]。
		cnn文件夹中包含三个基于CNN的sentence embedding模型文件，该文件被KBQA系统调用，用于语义分析[2]。
		dbqa文件夹包含五个样例模型文件，该文件被DBQA系统调用，用于计算question和answer sentence之间的relevance score。
	(4)training&testing
		该文件夹包含KBQA和DBQA两个任务在NLPCC2016上对应的训练文件和测试文件：
		nlpcc-iccpol-2016.kbqa.training-data for KBQA任务。
		nlpcc-iccpol-2016.dbqa.training-data for DBQA任务。
		nlpcc-iccpol-2016.kbqa.testing-data for KBQA任务。
		nlpcc-iccpol-2016.dbqa.testing-data for DBQA任务。
		nlpcc-iccpol-2017.tbqa.training-data for TBQA任务。
		nlpcc-iccpol-2017.tbqa.dev-data for TBQA任务。
		具体文件格式请参照NLPCC-ICCPOL-QA-2017.guideline.pdf。
		注意：NLPCC 2017 Open Domain QA三个子任务的测试集将在稍后发布，请大家关注NLPCC 2017官网。
	(5)tokenizer
		请参赛队伍自行加入中文分词功能，例如ICTCLAS发布的开源中文分词工具包：http://ictclas.nlpir.org/downloads。
	(6)evaltool
		该文件夹包含KBQA任务和DBQA任务计算评测指标工具及使用样例。
	
注意事项：
	(1)本评测工具包“仅限于学术使用，请勿用于任何商业用途”。
	(2)KBQA项目在加载知识库时，会占用较大的内存。请各个参赛队伍自行进行内存优化。
	(3)template、cnn和dbqa模型非常有限，仅供作为样例参考，请各个参赛队伍自行优化和改进。
	(4)我们非常鼓励参赛队伍能够使用自行开发的问答系统进行评测。本评测工具包仅供各个参赛队伍参考。
	(5)如有参赛队伍使用本评测工具包进行评测，那么我们鼓励在此基础上进行系统优化，如采用更复杂的特征和机器学习算法等。

联系人：
	段楠
	nanduan@microsoft.com

	唐都钰
	dutang@microsoft.com

modified @ 2017/03/31