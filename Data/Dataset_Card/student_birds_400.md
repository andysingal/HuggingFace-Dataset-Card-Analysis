鸟类400.物种图像分类
58388训练集，2000测试测试集，2000验证图像224X224X3 jpg格式

400种鸟类的数据集。58388张训练图像、2000张测试图像（每种5张图像）和2000张验证图像（每种5张图像）。这是一个非常高质量的数据集，每张图像中只有一只鸟，鸟通常占据图像中至少50%的像素。因此，即使是一个中等复杂的模型也能在90%的范围内实现训练和测试精度。

所有图像均为jpg格式的224 X 224 X 3彩色图像。数据集包括列车集、测试集和验证集。每套包含400个子目录，每种鸟类一个。如果使用Keras ImageDataGenerator，则数据结构非常方便。flowfromdirectory创建列车、测试和有效数据生成器。数据集还包括一个鸟类物种档案。csv。此cvs文件包含三列。“文件路径”列包含图像文件的文件路径。“标签”列包含与图像文件关联的类名。鸟类种类。如果使用df=pandas读入csv文件。birdscsv（Bird Species.csv）将创建一个pandas数据帧，然后可以将其拆分为traindf、testdf和validdf数据帧，以创建您自己的数据划分为train、test和validdf数据集。

注：数据集中的测试和验证图像是手工选择的“最佳”图像，因此使用这些数据集与创建自己的测试和验证集相比，您的模型可能会获得最高的准确度分数。然而，就看不见的图像上的模型性能而言，后一种情况更为准确。

这些图片是通过网络搜索按物种名称收集的。下载一个物种的图像文件后，使用我开发的python duplicate image detector程序检查其重复图像。删除所有检测到的重复项，以防止它们在训练集、测试集和验证集之间成为共同的图像。

之后，对图像进行裁剪，使鸟占据图像中至少50%的像素。然后，这些图像以jpg格式调整为224x224 X3。裁剪确保了当CNN对其进行处理时，图像中有足够的信息来创建高度准确的分类器。即使是一个中等稳健的模型，也应在高90%的范围内实现训练、验证和测试精度。由于数据集很大，我建议您尝试使用150 X 150 X3的模型和图像大小进行训练，以减少训练时间。所有文件也从每个物种的一个开始按顺序编号。所以测试图像被命名为1。jpg至5。jpg。对于验证图像也是如此。训练图像也用“零”填充顺序编号。例如001。jpg，002。jpg…010。jpg，011。jpg…。。099.jpg，100jpg，102。当与python文件函数和目录中的Keras流一起使用时，zero的填充保留了文件顺序。

训练集是不平衡的，每个物种有不同数量的文件。然而，每个物种至少有120个训练图像文件。这种不平衡并没有影响我的内核分类器，因为它在测试集上达到了98%以上的准确率。

数据集中一个显著的不平衡是雄性物种图像与雌性物种图像的比例。大约85%的图片是男性的，15%是女性的。典型的雄性动物的肤色要多样化得多，而一个物种的雌性动物通常是平淡无奇的。因此，男性和女性的形象可能看起来完全不同。几乎所有的测试和验证图像都来自该物种的雄性。因此，分类器可能无法在雌性物种图像上表现良好。