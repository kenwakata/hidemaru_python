#�G�ۃG�f�B�^��Python�𓮂����}�N��

##�T�v
�G�ۃG�f�B�^�ŕҏW���̃\�[�X�R�[�h��Python�Ŏ��s���܂��B

###�X�N���[���V���b�g�i���̂P�j
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161934.gif "Python �G�ۃG�f�B�^")
###�X�N���[���V���b�g�i���̂Q�j
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161912.gif "Python �G�ۃG�f�B�^")
###�X�N���[���V���b�g�i���̂R�j
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161852.gif "Python �G�ۃG�f�B�^")
###�X�N���[���V���b�g�i���̂S�j
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161838.gif "Python �G�ۃG�f�B�^")

###�C���X�g�[�����@
- �G�ۂ̃}�N���f�B���N�g���փR�s�[������L�[�A�T�C�����ĉ������B

##�����
- �G�ۃG�f�B�^ ver8.20 b14 �œ�����m�F�Aver8�ȍ~�Ȃ瓮���͂��B

###Python�o�[�W����
- �ǂ̃o�[�W�����ł������͂��ł��A���쌟�؂�Python ver2.7/ver3�n�ōs���Ă��܂��B
- �؂�ւ��̓}�N���`����$g_exe �ϐ���ҏW���ĉ������B

###����
�X�N���[���V���b�g�����Ă��炦�Ε����邩�Ǝv���܂����A���֐��̂��߁u�G���R�[�h�w��v�����Ă��܂��B
�G���R�[�h�w����s��Ȃ��Ă����{��(utf8/cp932�Ƃ�)���g���܂��B

���_�C���N�g�����Python���G���[�o�͂���̂ŁA�����������悤�Ƀ��_�C���N�g������Ă��܂��B
>UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-3: ordinal not in range(128)


�Ȃ̂ŁA���̃}�N���ł̓R�[�h�`���ŐF�X����Ă��܂��B

 
    �i�I���W�i���j
    print u"�ɂق�"
     
    �i���s�����R�[�h�j
    # -*- coding:utf8 -*-
    import sys, codecs
    sys.stdout = codecs.getwriter('cp932')(sys.stdout)
    del sys, codecs
    print u"�ɂق�"

�G���[�s��������Ă��܂�����p������܂����A�����R�[�h���v�������Ƃ�����������悤�ɕ֗�����D�悵�Ă��܂��B
