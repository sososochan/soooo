orfdo Sodbhuv = jdph:JhwVhuylfh("Sodbhuv")
orfdo UhsolfdwhgVwrudjh = jdph:JhwVhuylfh("UhsolfdwhgVwrudjh")
orfdo sodbhu = Sodbhuv.OrfdoSodbhu

orfdo DWWDFN_UDQJH = 60
orfdo DWWDFN_LQWHUYDO = 0.1

orfdo vfuhhqJxl = Lqvwdqfh.qhz("VfuhhqJxl")
vfuhhqJxl.Sduhqw = sodbhu:ZdlwIruFklog("SodbhuJxl")

orfdo iudph = Lqvwdqfh.qhz("Iudph")
iudph.Vlch = XGlp2.qhz(0, 200, 0, 100)
iudph.Srvlwlrq = XGlp2.qhz(0.5, -100, 0.5, -50)
iudph.Sduhqw = vfuhhqJxl

orfdo lqsxwEra = Lqvwdqfh.qhz("WhawEra")
lqsxwEra.Vlch = XGlp2.qhz(0, 180, 0, 30)
lqsxwEra.Srvlwlrq = XGlp2.qhz(0, 10, 0, 10)
lqsxwEra.SodfhkroghuWhaw = "Hqwhu Dwwdfn Udqjh"
lqsxwEra.Whaw = wrvwulqj(DWWDFN_UDQJH)
lqsxwEra.Sduhqw = iudph

orfdo xsgdwhExwwrq = Lqvwdqfh.qhz("WhawExwwrq")
xsgdwhExwwrq.Vlch = XGlp2.qhz(0, 180, 0, 30)
xsgdwhExwwrq.Srvlwlrq = XGlp2.qhz(0, 10, 0, 50)
xsgdwhExwwrq.Whaw = "Xsgdwh Udqjh"
xsgdwhExwwrq.Sduhqw = iudph

xsgdwhExwwrq.PrxvhExwwrq1Folfn:Frqqhfw(ixqfwlrq()
    orfdo lqsxwYdoxh = wrqxpehu(lqsxwEra.Whaw)
    li lqsxwYdoxh dqg lqsxwYdoxh > 0 wkhq
        DWWDFN_UDQJH = lqsxwYdoxh
        sulqw("Dwwdfn Udqjh xsgdwhg wr: " .. DWWDFN_UDQJH)
    hovh
        sulqw("Lqydolg lqsxw. Sohdvh hqwhu d ydolg qxpehu.")
    hqg
hqg)

orfdo ixqfwlrq JhwQhduebSodbhuv(fkdudfwhu, udqjh)
    orfdo wdujhwv = {}
    orfdo pbUrrw = fkdudfwhu:IlqgIluvwFklog("KxpdqrlgUrrwSduw")
    li qrw pbUrrw wkhq uhwxuq wdujhwv hqg

    iru _, rwkhu lq lsdluv(Sodbhuv:JhwSodbhuv()) gr
        li rwkhu ~= sodbhu dqg rwkhu.Fkdudfwhu dqg rwkhu.Fkdudfwhu:IlqgIluvwFklog("KxpdqrlgUrrwSduw") wkhq
            orfdo glvw = (rwkhu.Fkdudfwhu.KxpdqrlgUrrwSduw.Srvlwlrq - pbUrrw.Srvlwlrq).Pdjqlwxgh
            li glvw <= udqjh wkhq
                wdeoh.lqvhuw(wdujhwv, rwkhu.Fkdudfwhu)
            hqg
        hqg
    hqg
    uhwxuq wdujhwv
hqg

orfdo ixqfwlrq DwwdfnSodbhu(wdujhwFkdudfwhu)
    orfdo fkdudfwhu = sodbhu.Fkdudfwhu
    li qrw fkdudfwhu wkhq uhwxuq hqg

    orfdo htxlsshgZhdsrq
    iru _, lwhp lq lsdluv(fkdudfwhu:JhwFkloguhq()) gr
        li lwhp:LvD("Wrro") wkhq
            htxlsshgZhdsrq = lwhp
            euhdn
        hqg
    hqg
    li qrw htxlsshgZhdsrq wkhq uhwxuq hqg

    li htxlsshgZhdsrq:IlqgIluvwFklog("OhiwFolfnUhprwh") wkhq
        orfdo urrw = wdujhwFkdudfwhu:IlqgIluvwFklog("KxpdqrlgUrrwSduw")
        li urrw wkhq
            orfdo gluhfwlrq = (urrw.Srvlwlrq - fkdudfwhu:JhwSlyrw().Srvlwlrq).Xqlw
            sfdoo(ixqfwlrq()
                htxlsshgZhdsrq.OhiwFolfnUhprwh:IluhVhuyhu(gluhfwlrq, 1)
            hqg)
        hqg
    hovh
        orfdo khdg = wdujhwFkdudfwhu:IlqgIluvwFklog("Khdg")
        li khdg wkhq
            orfdo dwwdfnHyhqw = UhsolfdwhgVwrudjh:ZdlwIruFklog("Prgxohv"):ZdlwIruFklog("Qhw"):ZdlwIruFklog("UH/UhjlvwhuDwwdfn")
            orfdo klwHyhqw = UhsolfdwhgVwrudjh:ZdlwIruFklog("Prgxohv"):ZdlwIruFklog("Qhw"):ZdlwIruFklog("UH/UhjlvwhuKlw")
            sfdoo(ixqfwlrq()
                dwwdfnHyhqw:IluhVhuyhu(0.1)
                klwHyhqw:IluhVhuyhu(khdg, { {wdujhwFkdudfwhu, khdg} })
            hqg)
        hqg
    hqg
hqg

wdvn.vsdzq(ixqfwlrq()
    zkloh wuxh gr
        orfdo fkdudfwhu = sodbhu.Fkdudfwhu
        li fkdudfwhu wkhq
            orfdo hqhplhv = JhwQhduebSodbhuv(fkdudfwhu, DWWDFN_UDQJH)
            iru _, hqhpbFkdu lq lsdluv(hqhplhv) gr
                DwwdfnSodbhu(hqhpbFkdu)
            hqg
        hqg
        wdvn.zdlw(DWWDFN_LQWHUYDO)
    hqg
hqg)

orfdo gudjjlqj = idovh
orfdo gudjLqsxw
orfdo gudjVwduw
orfdo vwduwSrv

iudph.LqsxwEhjdq:Frqqhfw(ixqfwlrq(lqsxw)
    li lqsxw.XvhuLqsxwWbsh == Hqxp.XvhuLqsxwWbsh.Wrxfk wkhq
        gudjjlqj = wuxh
        gudjLqsxw = lqsxw
        gudjVwduw = lqsxw.Srvlwlrq
        vwduwSrv = iudph.Srvlwlrq
    hqg
hqg)

iudph.LqsxwFkdqjhg:Frqqhfw(ixqfwlrq(lqsxw)
    li gudjjlqj dqg lqsxw == gudjLqsxw wkhq
        orfdo ghowd = lqsxw.Srvlwlrq - gudjVwduw
        iudph.Srvlwlrq = XGlp2.qhz(vwduwSrv.A.Vfdoh, vwduwSrv.A.Riivhw + ghowd.A, vwduwSrv.B.Vfdoh, vwduwSrv.B.Riivhw + ghowd.B)
    hqg
hqg)

iudph.LqsxwHqghg:Frqqhfw(ixqfwlrq(lqsxw)
    li lqsxw == gudjLqsxw wkhq
        gudjjlqj = idovh
    hqg
hqg)
