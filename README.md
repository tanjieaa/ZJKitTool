# ZJUIKitTool
MVVM模式设计的图文混排评论列表，简单可随意更改的筛选视图，后期会不断完善，以及各个控件的封装，Block回调可以简单快速创建和使用Masonry布局，以及实现方法。还包括许多工具类的封装。

//比如快速创建一个按钮，并实现点击事件：

    [UIButton  zj_buttonWithTitle:@"评论列表" titleColor:kWhiteColor backColor:kOrangeColor fontSize:16 isBold:YES cornerRadius:3 supView:self.view constraints:^(MASConstraintMaker *make) {
        make.centerY.equalTo(chooseBtn.mas_centerY);
        make.left.equalTo(chooseBtn.mas_right).offset(50);
        make.width.mas_equalTo(100);
        make.height.mas_equalTo(40);
    } touchUp:^(id sender) {
        NSLog(@"这是按钮的点击事件");
    }];


//快速添加一个带placeholder的UITextView控件,并可以修改颜色

    [UITextView zj_textViewWithFontSize:16 textColor:[UIColor orangeColor] borderColor:k16RGBColor(0xCCCCCC) borderWidth:0.5 cornerRadiu:4 placeColor:k16RGBColor(0xBBBBBB) placeText:@"请输入..." superView:self.view constraints:^(MASConstraintMaker *make) {
        make.left.mas_equalTo(20);
        make.right.mas_equalTo(-20);
        make.bottom.mas_equalTo(-100);
        make.height.mas_equalTo(180);
    }];



请各位大神多多指教，多多支持点个Star。
