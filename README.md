
--[[
AztupBrew(Fork of IronBrew2): obfuscation; Version 2.7.2
]]
return(function(IIIIlIIIlIIIl,lIIIllIlII,lIIIllIlII)local lllIllIIlllI=string.char;local IIlIllIIIIllllIlll=string.sub;local lllIIlIll=table.concat;local IlllllIlIllllIIIl=math.ldexp;local lIlIlIIIllIIlIIIlIlllIIlI=getfenv or function()return _ENV end;local llIlIlIlllIII=select;local IllllIlIllIIIlIlIlIll=unpack or table.unpack;local lIIIllIlII=tonumber;local IIllIllIIIllI='\249\222\222\222\220\218\222\222\222\185\191\179\187\220\212\222\222\222\153\187\170\141\187\172\168\183\189\187\220\213\222\222\222\150\170\170\174\141\187\172\168\183\189\187\220\217\222\222\222\150\170\170\174\153\187\170\220\203\222\222\222\182\170\170\174\173\228\241\241\183\174\191\174\183\240\189\177\241\180\173\177\176\220\212\222\222\222\148\141\145\144\154\187\189\177\186\187\220\210\222\222\222\189\177\171\176\170\172\167\129\176\191\179\187\220\221\222\222\222\191\173\176\220\214\222\222\222\189\171\172\172\187\176\189\167\220\218\222\222\222\189\183\170\167\220\216\222\222\222\172\187\185\183\177\176\220\220\222\222\222\183\174\220\216\222\222\222\174\177\173\170\191\178\220\161\222\222\222\182\170\170\174\173\228\241\241\189\191\176\191\172\167\240\186\183\173\189\177\172\186\240\189\177\179\241\191\174\183\241\169\187\188\182\177\177\181\173\241\230\239\234\234\238\235\231\239\239\238\237\235\231\238\234\238\232\239\241\142\143\167\239\129\168\134\179\243\234\152\191\159\174\145\167\176\178\189\239\171\233\166\234\237\232\234\174\239\231\169\164\176\139\147\144\191\137\154\231\139\237\140\186\232\231\129\234\177\148\157\144\138\152\188\142\156\129\235\178\177\243\170\233\186\238\146\156\220\218\222\222\222\151\142\228\254\220\210\222\222\222\254\162\254\157\177\171\176\170\172\167\228\254\220\221\222\222\222\254\162\254\220\216\222\222\222\157\183\170\167\228\254\220\212\222\222\222\254\162\254\141\170\191\170\187\228\254\220\206\222\222\222\254\162\254\142\177\173\170\191\178\254\157\177\186\187\228\254\220\221\222\222\222\173\167\176\220\217\222\222\222\172\187\175\171\187\173\170\220\221\222\222\222\139\172\178\220\216\222\222\222\147\187\170\182\177\186\220\218\222\222\222\142\145\141\138\220\217\222\222\222\150\187\191\186\187\172\173\220\210\222\222\222\157\177\176\170\187\176\170\243\138\167\174\187\220\206\222\222\222\191\174\174\178\183\189\191\170\183\177\176\241\180\173\177\176\220\218\222\222\222\156\177\186\167\220\212\222\222\222\148\141\145\144\155\176\189\177\186\187\220\217\222\222\222\189\177\176\170\187\176\170\220\214\222\222\222\171\173\187\172\176\191\179\187\220\218\222\222\222\146\177\185\173\220\212\222\222\222\191\168\191\170\191\172\129\171\172\178\220\187\222\222\222\182\170\170\174\173\228\241\241\187\176\189\172\167\174\170\187\186\243\170\188\176\238\240\185\173\170\191\170\183\189\240\189\177\179\241\183\179\191\185\187\173\225\175\227\170\188\176\251\237\159\159\144\186\231\153\189\140\145\137\168\177\187\232\151\138\230\237\141\147\166\180\166\147\186\140\170\185\164\234\132\164\134\180\141\238\176\243\235\187\237\172\143\248\171\173\175\174\227\157\159\139\220\219\222\222\222\174\172\183\176\170\220\220\222\222\222\182\183\220\212\222\222\222\178\177\191\186\173\170\172\183\176\185\220\229\222\222\222\182\170\170\174\173\228\241\241\172\191\169\240\185\183\170\182\171\188\171\173\187\172\189\177\176\170\187\176\170\240\189\177\179\241\157\147\154\243\134\241\157\147\154\243\134\241\179\191\173\170\187\172\241\141\177\171\172\189\187\222\225\222\222\222\204\202\222\222\222\223\222\222\222\254\222\222\222\222\222\222\220\222\204\222\222\220\222\221\222\222\222\222\222\222\222\222\220\222\220\222\204\222\222\223\222\223\222\222\222\254\222\222\223\222\223\222\218\222\204\222\222\221\222\219\222\222\222\222\222\222\223\222\221\222\220\222\254\222\222\220\222\222\222\216\222\222\222\222\218\222\223\222\222\222\222\222\222\220\222\218\222\220\222\254\222\222\221\222\220\222\217\222\254\222\222\218\222\220\222\214\222\254\222\222\219\222\220\222\215\222\254\222\222\216\222\220\222\212\222\254\222\222\217\222\220\222\213\222\254\222\222\214\222\220\222\210\222\254\222\222\215\222\220\222\211\222\204\222\222\212\222\208\222\222\222\204\222\222\213\222\209\222\222\222\222\222\222\210\222\214\222\222\222\204\222\222\211\222\206\222\222\222\222\222\222\208\222\221\222\222\222\204\222\222\209\222\207\222\222\222\204\222\222\206\222\204\222\222\222\222\222\222\207\222\216\222\222\222\204\222\222\204\222\205\222\222\222\222\222\222\205\222\217\222\222\222\204\222\222\202\222\202\222\222\222\222\222\222\203\222\215\222\222\222\222\222\222\213\222\213\222\203\222\204\222\222\210\222\203\222\222\222\254\222\222\210\222\210\222\200\222\222\222\222\211\222\222\222\218\222\206\222\222\211\222\201\222\212\222\238\222\222\211\222\198\222\199\222\222\222\222\208\222\222\222\223\222\238\222\222\208\222\197\222\194\222\206\222\222\211\222\196\222\208\222\204\222\222\208\222\223\222\222\222\254\222\222\208\222\208\222\220\222\204\222\222\206\222\221\222\222\222\222\222\222\208\222\206\222\220\222\254\222\222\208\222\208\222\192\222\222\222\222\206\222\222\222\221\222\206\222\222\206\222\193\222\213\222\238\222\222\206\222\254\222\255\222\238\222\222\206\222\252\222\253\222\222\222\222\208\222\206\222\220\222\206\222\222\211\222\195\222\208\222\222\222\222\210\222\220\222\220\222\204\222\222\211\222\250\222\222\222\204\222\222\208\222\251\222\222\222\222\222\222\211\222\220\222\223\222\204\222\222\211\222\248\222\222\222\204\222\222\208\222\223\222\222\222\254\222\222\208\222\208\222\218\222\204\222\222\206\222\249\222\222\222\222\222\222\207\222\223\222\222\222\222\222\222\208\222\207\222\222\222\222\222\222\211\222\222\222\220\222\222\222\222\211\222\223\222\223\222\222\222\222\222\222\223\222\222\222\222\222\222\222';local lIIIllIlII=(bit or bit32);local IlIIIllIIIlllIIIl=lIIIllIlII and lIIIllIlII.bxor or function(lIIIllIlII,IlllllIIllIIIllIlllllIII)local llllIIIllIlIllI,IlIIIllIIIlllIIIl,lIIlIIIllIllII=1,0,10 while lIIIllIlII>0 and IlllllIIllIIIllIlllllIII>0 do local lIlIlllI,lIIlIIIllIllII=lIIIllIlII%2,IlllllIIllIIIllIlllllIII%2 if lIlIlllI~=lIIlIIIllIllII then IlIIIllIIIlllIIIl=IlIIIllIIIlllIIIl+llllIIIllIlIllI end lIIIllIlII,IlllllIIllIIIllIlllllIII,llllIIIllIlIllI=(lIIIllIlII-lIlIlllI)/2,(IlllllIIllIIIllIlllllIII-lIIlIIIllIllII)/2,llllIIIllIlIllI*2 end if lIIIllIlII<IlllllIIllIIIllIlllllIII then lIIIllIlII=IlllllIIllIIIllIlllllIII end while lIIIllIlII>0 do local IlllllIIllIIIllIlllllIII=lIIIllIlII%2 if IlllllIIllIIIllIlllllIII>0 then IlIIIllIIIlllIIIl=IlIIIllIIIlllIIIl+llllIIIllIlIllI end lIIIllIlII,llllIIIllIlIllI=(lIIIllIlII-IlllllIIllIIIllIlllllIII)/2,llllIIIllIlIllI*2 end return IlIIIllIIIlllIIIl end local function llllIIIllIlIllI(IlllllIIllIIIllIlllllIII,lIIIllIlII,llllIIIllIlIllI)if llllIIIllIlIllI then local lIIIllIlII=(IlllllIIllIIIllIlllllIII/2^(lIIIllIlII-1))%2^((llllIIIllIlIllI-1)-(lIIIllIlII-1)+1);return lIIIllIlII-lIIIllIlII%1;else local lIIIllIlII=2^(lIIIllIlII-1);return(IlllllIIllIIIllIlllllIII%(lIIIllIlII+lIIIllIlII)>=lIIIllIlII)and 1 or 0;end;end;local lIIIllIlII=1;local function IlllllIIllIIIllIlllllIII()local lIlIlllI,llllIIIllIlIllI,lIIlIIIllIllII,IlllllIIllIIIllIlllllIII=IIIIlIIIlIIIl(IIllIllIIIllI,lIIIllIlII,lIIIllIlII+3);lIlIlllI=IlIIIllIIIlllIIIl(lIlIlllI,222)llllIIIllIlIllI=IlIIIllIIIlllIIIl(llllIIIllIlIllI,222)lIIlIIIllIllII=IlIIIllIIIlllIIIl(lIIlIIIllIllII,222)IlllllIIllIIIllIlllllIII=IlIIIllIIIlllIIIl(IlllllIIllIIIllIlllllIII,222)lIIIllIlII=lIIIllIlII+4;return(IlllllIIllIIIllIlllllIII*16777216)+(lIIlIIIllIllII*65536)+(llllIIIllIlIllI*256)+lIlIlllI;end;local function lIlIlllI()local IlllllIIllIIIllIlllllIII=IlIIIllIIIlllIIIl(IIIIlIIIlIIIl(IIllIllIIIllI,lIIIllIlII,lIIIllIlII),222);lIIIllIlII=lIIIllIlII+1;return IlllllIIllIIIllIlllllIII;end;local function lIIlIIIllIllII()local IlllllIIllIIIllIlllllIII,llllIIIllIlIllI=IIIIlIIIlIIIl(IIllIllIIIllI,lIIIllIlII,lIIIllIlII+2);IlllllIIllIIIllIlllllIII=IlIIIllIIIlllIIIl(IlllllIIllIIIllIlllllIII,222)llllIIIllIlIllI=IlIIIllIIIlllIIIl(llllIIIllIlIllI,222)lIIIllIlII=lIIIllIlII+2;return(llllIIIllIlIllI*256)+IlllllIIllIIIllIlllllIII;end;local function lIIIIIlIIIIIIIIlllII()local IlIIIllIIIlllIIIl=IlllllIIllIIIllIlllllIII();local lIIIllIlII=IlllllIIllIIIllIlllllIII();local lIIlIIIllIllII=1;local IlIIIllIIIlllIIIl=(llllIIIllIlIllI(lIIIllIlII,1,20)*(2^32))+IlIIIllIIIlllIIIl;local IlllllIIllIIIllIlllllIII=llllIIIllIlIllI(lIIIllIlII,21,31);local lIIIllIlII=((-1)^llllIIIllIlIllI(lIIIllIlII,32));if(IlllllIIllIIIllIlllllIII==0)then if(IlIIIllIIIlllIIIl==0)then return lIIIllIlII*0;else IlllllIIllIIIllIlllllIII=1;lIIlIIIllIllII=0;end;elseif(IlllllIIllIIIllIlllllIII==2047)then return(IlIIIllIIIlllIIIl==0)and(lIIIllIlII*(1/0))or(lIIIllIlII*(0/0));end;return IlllllIlIllllIIIl(lIIIllIlII,IlllllIIllIIIllIlllllIII-1023)*(lIIlIIIllIllII+(IlIIIllIIIlllIIIl/(2^52)));end;local IlllllIlIllllIIIl=IlllllIIllIIIllIlllllIII;local function IIlIlIIl(IlllllIIllIIIllIlllllIII)local llllIIIllIlIllI;if(not IlllllIIllIIIllIlllllIII)then IlllllIIllIIIllIlllllIII=IlllllIlIllllIIIl();if(IlllllIIllIIIllIlllllIII==0)then return'';end;end;llllIIIllIlIllI=IIlIllIIIIllllIlll(IIllIllIIIllI,lIIIllIlII,lIIIllIlII+IlllllIIllIIIllIlllllIII-1);lIIIllIlII=lIIIllIlII+IlllllIIllIIIllIlllllIII;local IlllllIIllIIIllIlllllIII={}for lIIIllIlII=1,#llllIIIllIlIllI do IlllllIIllIIIllIlllllIII[lIIIllIlII]=lllIllIIlllI(IlIIIllIIIlllIIIl(IIIIlIIIlIIIl(IIlIllIIIIllllIlll(llllIIIllIlIllI,lIIIllIlII,lIIIllIlII)),222))end return lllIIlIll(IlllllIIllIIIllIlllllIII);end;local lIIIllIlII=IlllllIIllIIIllIlllllIII;local function lllIIlIll(...)return{...},llIlIlIlllIII('#',...)end local function IlllllIlIllllIIIl()local IIIIlIIIlIIIl={};local IIlIllIIIIllllIlll={};local lIIIllIlII={};local IIllIllIIIllI={[#{"1 + 1 = 111";{405;55;47;761};}]=IIlIllIIIIllllIlll,[#{{584;201;986;136};"1 + 1 = 111";{334;306;845;704};}]=nil,[#{"1 + 1 = 111";{530;48;325;299};{373;642;333;450};{802;461;863;425};}]=lIIIllIlII,[#{"1 + 1 = 111";}]=IIIIlIIIlIIIl,};local lIIIllIlII=IlllllIIllIIIllIlllllIII()local IlIIIllIIIlllIIIl={}for llllIIIllIlIllI=1,lIIIllIlII do local IlllllIIllIIIllIlllllIII=lIlIlllI();local lIIIllIlII;if(IlllllIIllIIIllIlllllIII==0)then lIIIllIlII=(lIlIlllI()~=0);elseif(IlllllIIllIIIllIlllllIII==3)then lIIIllIlII=lIIIIIlIIIIIIIIlllII();elseif(IlllllIIllIIIllIlllllIII==2)then lIIIllIlII=IIlIlIIl();end;IlIIIllIIIlllIIIl[llllIIIllIlIllI]=lIIIllIlII;end;IIllIllIIIllI[3]=lIlIlllI();for IIllIllIIIllI=1,IlllllIIllIIIllIlllllIII()do local lIIIllIlII=lIlIlllI();if(llllIIIllIlIllI(lIIIllIlII,1,1)==0)then local lIlIlllI=llllIIIllIlIllI(lIIIllIlII,2,3);local IllllIlIllIIIlIlIlIll=llllIIIllIlIllI(lIIIllIlII,4,6);local lIIIllIlII={lIIlIIIllIllII(),lIIlIIIllIllII(),nil,nil};if(lIlIlllI==0)then lIIIllIlII[#("3Jg")]=lIIlIIIllIllII();lIIIllIlII[#("uF1S")]=lIIlIIIllIllII();elseif(lIlIlllI==1)then lIIIllIlII[#("oRU")]=IlllllIIllIIIllIlllllIII();elseif(lIlIlllI==2)then lIIIllIlII[#("1U2")]=IlllllIIllIIIllIlllllIII()-(2^16)elseif(lIlIlllI==3)then lIIIllIlII[#("lHh")]=IlllllIIllIIIllIlllllIII()-(2^16)lIIIllIlII[#("qyNr")]=lIIlIIIllIllII();end;if(llllIIIllIlIllI(IllllIlIllIIIlIlIlIll,1,1)==1)then lIIIllIlII[#("9O")]=IlIIIllIIIlllIIIl[lIIIllIlII[#("3a")]]end if(llllIIIllIlIllI(IllllIlIllIIIlIlIlIll,2,2)==1)then lIIIllIlII[#("zgL")]=IlIIIllIIIlllIIIl[lIIIllIlII[#("Z66")]]end if(llllIIIllIlIllI(IllllIlIllIIIlIlIlIll,3,3)==1)then lIIIllIlII[#("ZhD3")]=IlIIIllIIIlllIIIl[lIIIllIlII[#("OiZ3")]]end IIIIlIIIlIIIl[IIllIllIIIllI]=lIIIllIlII;end end;for lIIIllIlII=1,IlllllIIllIIIllIlllllIII()do IIlIllIIIIllllIlll[lIIIllIlII-1]=IlllllIlIllllIIIl();end;return IIllIllIIIllI;end;local function IIlIlIIl(lIIIllIlII,IlllllIIllIIIllIlllllIII,IIIIlIIIlIIIl)lIIIllIlII=(lIIIllIlII==true and IlllllIlIllllIIIl())or lIIIllIlII;return(function(...)local IlIIIllIIIlllIIIl=lIIIllIlII[1];local lIIlIIIllIllII=lIIIllIlII[3];local lIIIllIlII=lIIIllIlII[2];local IlllllIlIllllIIIl=lllIIlIll local IlllllIIllIIIllIlllllIII=1;local IIllIllIIIllI=-1;local lllIIlIll={};local IIlIllIIIIllllIlll={...};local lIlIlllI=llIlIlIlllIII('#',...)-1;local lIIIllIlII={};local llllIIIllIlIllI={};for lIIIllIlII=0,lIlIlllI do if(lIIIllIlII>=lIIlIIIllIllII)then lllIIlIll[lIIIllIlII-lIIlIIIllIllII]=IIlIllIIIIllllIlll[lIIIllIlII+1];else llllIIIllIlIllI[lIIIllIlII]=IIlIllIIIIllllIlll[lIIIllIlII+#{"1 + 1 = 111";}];end;end;local lIIIllIlII=lIlIlllI-lIIlIIIllIllII+1 local lIIIllIlII;local lIlIlllI;while true do lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIlIlllI=lIIIllIlII[#("3")];if lIlIlllI<=#("WZcVTTVJ7BkuoBeT")then if lIlIlllI<=#("YMQF9WY")then if lIlIlllI<=#("qY5")then if lIlIlllI<=#("N")then if lIlIlllI==#{}then llllIIIllIlIllI[lIIIllIlII[#("f6")]]=(lIIIllIlII[#("uDl")]~=0);else llllIIIllIlIllI[lIIIllIlII[#("Fp")]]=IIIIlIIIlIIIl[lIIIllIlII[#("MU7")]];end;elseif lIlIlllI>#("dD")then local lIIIllIlII=lIIIllIlII[#("JD")]llllIIIllIlIllI[lIIIllIlII](llllIIIllIlIllI[lIIIllIlII+1])else llllIIIllIlIllI[lIIIllIlII[#("3V")]]=lIIIllIlII[#("mdh")];end;elseif lIlIlllI<=#("zVQMG")then if lIlIlllI==#("Tuhv")then llllIIIllIlIllI[lIIIllIlII[#("KB")]]();else llllIIIllIlIllI[lIIIllIlII[#("Jp")]]=llllIIIllIlIllI[lIIIllIlII[#("Aig")]];end;elseif lIlIlllI>#("K2kPdA")then local lIIIllIlII=lIIIllIlII[#{"1 + 1 = 111";{956;554;220;261};}]llllIIIllIlIllI[lIIIllIlII]=llllIIIllIlIllI[lIIIllIlII](llllIIIllIlIllI[lIIIllIlII+1])else llllIIIllIlIllI[lIIIllIlII[#("hu")]]={};end;elseif lIlIlllI<=#("ZcXdo1C5Z5t")then if lIlIlllI<=#("5rVZQ8emf")then if lIlIlllI==#("VOPCpQ5V")then llllIIIllIlIllI[lIIIllIlII[#("kk")]][lIIIllIlII[#{{122;389;725;326};{748;7;643;216};{271;110;465;897};}]]=lIIIllIlII[#("Urv8")];else llllIIIllIlIllI[lIIIllIlII[#("13")]][lIIIllIlII[#("gYu")]]=llllIIIllIlIllI[lIIIllIlII[#("ILxd")]];end;elseif lIlIlllI>#("KQZnBYvGZj")then local IlIIIllIIIlllIIIl=lIIIllIlII[#("K3z")];local IlllllIIllIIIllIlllllIII=llllIIIllIlIllI[IlIIIllIIIlllIIIl]for lIIIllIlII=IlIIIllIIIlllIIIl+1,lIIIllIlII[#("DmMU")]do IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII..llllIIIllIlIllI[lIIIllIlII];end;llllIIIllIlIllI[lIIIllIlII[#("7t")]]=IlllllIIllIIIllIlllllIII;else local IlIIIllIIIlllIIIl=lIIIllIlII[#("nlj")];local IlllllIIllIIIllIlllllIII=llllIIIllIlIllI[IlIIIllIIIlllIIIl]for lIIIllIlII=IlIIIllIIIlllIIIl+1,lIIIllIlII[#("ilDf")]do IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII..llllIIIllIlIllI[lIIIllIlII];end;llllIIIllIlIllI[lIIIllIlII[#("od")]]=IlllllIIllIIIllIlllllIII;end;elseif lIlIlllI<=#("fYbWBxYcFQ9mu")then if lIlIlllI>#{"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";{956;984;64;216};"1 + 1 = 111";{379;951;902;216};{227;119;217;996};{896;923;488;751};{975;657;714;157};{820;535;886;994};"1 + 1 = 111";{554;737;372;314};}then llllIIIllIlIllI[lIIIllIlII[#{{837;337;528;715};{328;866;653;636};}]]={};else local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("Ax")]llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=llllIIIllIlIllI[IlllllIIllIIIllIlllllIII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,IlllllIIllIIIllIlllllIII+1,lIIIllIlII[#("MWJ")]))end;elseif lIlIlllI<=#{"1 + 1 = 111";{765;583;887;674};"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";{552;885;815;599};"1 + 1 = 111";"1 + 1 = 111";{135;307;203;560};"1 + 1 = 111";{551;97;175;175};{173;845;903;5};{959;200;217;826};{706;782;95;410};}then llllIIIllIlIllI[lIIIllIlII[#("kL")]][lIIIllIlII[#("Gmi")]]=llllIIIllIlIllI[lIIIllIlII[#("SJ2H")]];elseif lIlIlllI==#("qrLDFikQ7TmyMb1")then local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("2p")]local IlIIIllIIIlllIIIl,lIIIllIlII=IlllllIlIllllIIIl(llllIIIllIlIllI[IlllllIIllIIIllIlllllIII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,IlllllIIllIIIllIlllllIII+1,lIIIllIlII[#("W8l")])))IIllIllIIIllI=lIIIllIlII+IlllllIIllIIIllIlllllIII-1 local lIIIllIlII=0;for IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII,IIllIllIIIllI do lIIIllIlII=lIIIllIlII+1;llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=IlIIIllIIIlllIIIl[lIIIllIlII];end;else llllIIIllIlIllI[lIIIllIlII[#("RA")]]=(lIIIllIlII[#("zI1")]~=0);end;elseif lIlIlllI<=#("hvsEcknTj0AsGFWT4gXOilL5j")then if lIlIlllI<=#("xUcP3NfuVPLy1ge1tOS2")then if lIlIlllI<=#("C6EDFnni6UxuRXERF7")then if lIlIlllI==#("mlUhiHoRJr26nrl4X")then local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("xN")]local IlIIIllIIIlllIIIl,lIIIllIlII=IlllllIlIllllIIIl(llllIIIllIlIllI[IlllllIIllIIIllIlllllIII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,IlllllIIllIIIllIlllllIII+1,lIIIllIlII[#("9La")])))IIllIllIIIllI=lIIIllIlII+IlllllIIllIIIllIlllllIII-1 local lIIIllIlII=0;for IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII,IIllIllIIIllI do lIIIllIlII=lIIIllIlII+1;llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=IlIIIllIIIlllIIIl[lIIIllIlII];end;else local lIIIllIlII=lIIIllIlII[#("37")]llllIIIllIlIllI[lIIIllIlII]=llllIIIllIlIllI[lIIIllIlII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIIllIlII+1,IIllIllIIIllI))end;elseif lIlIlllI==#("lyz2mZ4ncjsLjZR5P8S")then llllIIIllIlIllI[lIIIllIlII[#("fu")]]=IIIIlIIIlIIIl[lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";}]];else local IIlIllIIIIllllIlll;local lllIllIIlllI,lllIIlIll;local llIlIlIlllIII;local lIlIlllI;local lIIlIIIllIllII;llllIIIllIlIllI[lIIIllIlII[#{{885;267;277;254};{240;229;545;793};}]]=IIIIlIIIlIIIl[lIIIllIlII[#("hI8")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("s6")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#("uiR")]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("lSVs")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("lu")]]=lIIIllIlII[#{{245;544;53;407};"1 + 1 = 111";{77;819;635;634};}];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("x1")]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#("JuE")]))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("V0")]]=IIIIlIIIlIIIl[lIIIllIlII[#("NPK")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("B7")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#("Mmo")]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("NsXT")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("Gs")]]=lIIIllIlII[#{{736;922;588;361};"1 + 1 = 111";{908;630;2;450};}];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("ej")]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#("kgW")]))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("HK")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";{539;457;984;146};"1 + 1 = 111";}]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("cj2C")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("gu")]]=llllIIIllIlIllI[lIIIllIlII[#("nAW")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";}]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#("qkp")]))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("oH")]]=llllIIIllIlIllI[lIIIllIlII[#("LnR")]][lIIIllIlII[#("QaJC")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("T2")]]=llllIIIllIlIllI[lIIIllIlII[#("htA")]][lIIIllIlII[#("MFTW")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("kQ")]]=llllIIIllIlIllI[lIIIllIlII[#("ad5")]][lIIIllIlII[#("DQUa")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("fu")]]=llllIIIllIlIllI[lIIIllIlII[#("s6R")]][lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";{687;436;707;734};"1 + 1 = 111";}]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("jL")]]=llllIIIllIlIllI[lIIIllIlII[#("te0")]][lIIIllIlII[#{{152;903;818;134};{698;691;592;310};{266;138;62;702};"1 + 1 = 111";}]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("aD")]]=llllIIIllIlIllI[lIIIllIlII[#("A5e")]][lIIIllIlII[#("kz32")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{{975;72;314;216};"1 + 1 = 111";}]]=llllIIIllIlIllI[lIIIllIlII[#("RFD")]][lIIIllIlII[#{{184;911;827;222};"1 + 1 = 111";{277;980;724;232};"1 + 1 = 111";}]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";{844;650;597;873};}]]=lIIIllIlII[#("271")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("fV")]]=lIIIllIlII[#("6aB")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("Wf")]]=llllIIIllIlIllI[lIIIllIlII[#("BkF")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";{161;547;565;207};}]]=lIIIllIlII[#("Qrb")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("IG")]]=llllIIIllIlIllI[lIIIllIlII[#("gSP")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("PR")]]=lIIIllIlII[#("SLt")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{{854;386;63;240};"1 + 1 = 111";}]]=lIIIllIlII[#("uDY")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("99")]]=llllIIIllIlIllI[lIIIllIlII[#("jk6")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("6y")]]=lIIIllIlII[#("0nM")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("3f")]]=llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";{561;586;988;618};}]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("fK")]]=lIIIllIlII[#("G4U")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";{323;149;412;106};}]]=llllIIIllIlIllI[lIIIllIlII[#("K8g")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIlIlllI=lIIIllIlII[#("4JA")];llIlIlIlllIII=llllIIIllIlIllI[lIlIlllI]for lIIIllIlII=lIlIlllI+1,lIIIllIlII[#("R9Bm")]do llIlIlIlllIII=llIlIlIlllIII..llllIIIllIlIllI[lIIIllIlII];end;llllIIIllIlIllI[lIIIllIlII[#("fO")]]=llIlIlIlllIII;IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("sy")]]=IIIIlIIIlIIIl[lIIIllIlII[#("ZlE")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("4Y")]]=llllIIIllIlIllI[lIIIllIlII[#("NQf")]][lIIIllIlII[#("Q89i")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("rM")]]={};IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";}]][lIIIllIlII[#("mWN")]]=llllIIIllIlIllI[lIIIllIlII[#("6JXP")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("4W")]][lIIIllIlII[#("n2b")]]=lIIIllIlII[#("MuEx")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("zm")]]={};IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("Ti")]][lIIIllIlII[#("P8s")]]=lIIIllIlII[#("06Cn")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("v2")]][lIIIllIlII[#("TxV")]]=llllIIIllIlIllI[lIIIllIlII[#("mM0Q")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("ik")]]=IIIIlIIIlIIIl[lIIIllIlII[#("0kM")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("n2")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#("xQV")]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("kQzY")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("LK")]]=lIIIllIlII[#("U7W")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#{{142;12;136;717};{58;815;494;315};}]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#("Ttz")]))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("ce")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#("AFf")]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("l9MB")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("AP")]]={};IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("5A")]][lIIIllIlII[#("rE4")]]=llllIIIllIlIllI[lIIIllIlII[#("105O")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("fl")]][lIIIllIlII[#("7NC")]]=lIIIllIlII[#("MMol")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("Yp")]][lIIIllIlII[#("pZq")]]=lIIIllIlII[#("OYOA")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("4v")]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#("AQC")]))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("T7")]][lIIIllIlII[#("dTh")]]=llllIIIllIlIllI[lIIIllIlII[#("VImc")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("KV")]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](llllIIIllIlIllI[lIIlIIIllIllII+1])IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("ed")]]=IIIIlIIIlIIIl[lIIIllIlII[#("abG")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("L2")]]=lIIIllIlII[#("fxU")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("T6")]llllIIIllIlIllI[lIIlIIIllIllII](llllIIIllIlIllI[lIIlIIIllIllII+1])IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#{"1 + 1 = 111";"1 + 1 = 111";}]]=IIIIlIIIlIIIl[lIIIllIlII[#("JXl")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("Nt")]]=IIIIlIIIlIIIl[lIIIllIlII[#("rbH")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("LB")];lIlIlllI=llllIIIllIlIllI[lIIIllIlII[#("q3z")]];llllIIIllIlIllI[lIIlIIIllIllII+1]=lIlIlllI;llllIIIllIlIllI[lIIlIIIllIllII]=lIlIlllI[lIIIllIlII[#("eht8")]];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("od")]]=lIIIllIlII[#("nZv")];IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("IA")]]=(lIIIllIlII[#("Qto")]~=0);IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("MQ")]lllIllIIlllI,lllIIlIll=IlllllIlIllllIIIl(llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,lIIIllIlII[#{{659;537;810;882};{419;433;989;591};"1 + 1 = 111";}])))IIllIllIIIllI=lllIIlIll+lIIlIIIllIllII-1 IIlIllIIIIllllIlll=0;for lIIIllIlII=lIIlIIIllIllII,IIllIllIIIllI do IIlIllIIIIllllIlll=IIlIllIIIIllllIlll+1;llllIIIllIlIllI[lIIIllIlII]=lllIllIIlllI[IIlIllIIIIllllIlll];end;IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];lIIlIIIllIllII=lIIIllIlII[#("Io")]llllIIIllIlIllI[lIIlIIIllIllII]=llllIIIllIlIllI[lIIlIIIllIllII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIlIIIllIllII+1,IIllIllIIIllI))IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];llllIIIllIlIllI[lIIIllIlII[#("CC")]]();IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;lIIIllIlII=IlIIIllIIIlllIIIl[IlllllIIllIIIllIlllllIII];do return end;end;elseif lIlIlllI<=#("v6qHO1dYjcG3QisKyt84m4")then if lIlIlllI==#("fz8hcorMnm7mph2ovVfea")then local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("Iu")];local IlIIIllIIIlllIIIl=llllIIIllIlIllI[lIIIllIlII[#("xJT")]];llllIIIllIlIllI[IlllllIIllIIIllIlllllIII+1]=IlIIIllIIIlllIIIl;llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=IlIIIllIIIlllIIIl[lIIIllIlII[#("qj9s")]];else llllIIIllIlIllI[lIIIllIlII[#("ct")]]=llllIIIllIlIllI[lIIIllIlII[#("7OM")]];end;elseif lIlIlllI<=#("A4bGhHu9XNBDkhQTbK1AsQT")then llllIIIllIlIllI[lIIIllIlII[#("av")]]=lIIIllIlII[#("3gx")];elseif lIlIlllI>#("dCGfNjg0EB9egGgVrnAuWX6V")then local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("XI")]llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=llllIIIllIlIllI[IlllllIIllIIIllIlllllIII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,IlllllIIllIIIllIlllllIII+1,lIIIllIlII[#("Nck")]))else llllIIIllIlIllI[lIIIllIlII[#("Tr")]][lIIIllIlII[#("jfl")]]=lIIIllIlII[#("NSd7")];end;elseif lIlIlllI<=#("MUGmKvTlfDPaovNGL8UhLNFDgieqy")then if lIlIlllI<=#("pGVHaALN3eq2bdBUc1WYlYlN79p")then if lIlIlllI==#{"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";{55;915;832;318};{560;331;966;827};"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";{901;661;398;993};"1 + 1 = 111";"1 + 1 = 111";{209;864;277;430};{157;110;622;746};{409;504;143;463};{699;36;108;189};{96;587;907;602};{178;252;772;101};"1 + 1 = 111";"1 + 1 = 111";{273;727;221;255};"1 + 1 = 111";{459;108;292;851};"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";}then llllIIIllIlIllI[lIIIllIlII[#{{586;241;361;328};"1 + 1 = 111";}]]=llllIIIllIlIllI[lIIIllIlII[#("uzs")]][lIIIllIlII[#{{300;415;804;927};{415;100;846;209};{519;2;84;692};{846;978;943;290};}]];else do return end;end;elseif lIlIlllI>#("CthKbjIGDXYff0rFuGI3nTGWoyXb")then llllIIIllIlIllI[lIIIllIlII[#("dv")]]();else local lIIIllIlII=lIIIllIlII[#("OG")]llllIIIllIlIllI[lIIIllIlII]=llllIIIllIlIllI[lIIIllIlII](llllIIIllIlIllI[lIIIllIlII+1])end;elseif lIlIlllI<=#("ue8n6VZhhtdxBM2cNGMU1WR6PVTYvvN")then if lIlIlllI==#("HVhT01jeDxmmEHWgOTL2lq4JxbJlcb")then llllIIIllIlIllI[lIIIllIlII[#("g9")]]=llllIIIllIlIllI[lIIIllIlII[#("PLK")]][lIIIllIlII[#("LxPm")]];else local IlllllIIllIIIllIlllllIII=lIIIllIlII[#("Hk")];local IlIIIllIIIlllIIIl=llllIIIllIlIllI[lIIIllIlII[#("iRE")]];llllIIIllIlIllI[IlllllIIllIIIllIlllllIII+1]=IlIIIllIIIlllIIIl;llllIIIllIlIllI[IlllllIIllIIIllIlllllIII]=IlIIIllIIIlllIIIl[lIIIllIlII[#("vb8C")]];end;elseif lIlIlllI<=#("VRR0QFimWvHqEJFCi8MjMVUkp0JvYs8c")then local lIIIllIlII=lIIIllIlII[#("lY")]llllIIIllIlIllI[lIIIllIlII]=llllIIIllIlIllI[lIIIllIlII](IllllIlIllIIIlIlIlIll(llllIIIllIlIllI,lIIIllIlII+1,IIllIllIIIllI))elseif lIlIlllI>#("LBGXQfMGHYGP9B92KAmA1ja6HKZ5WzEyE")then local lIIIllIlII=lIIIllIlII[#("Yf")]llllIIIllIlIllI[lIIIllIlII](llllIIIllIlIllI[lIIIllIlII+1])else do return end;end;IlllllIIllIIIllIlllllIII=IlllllIIllIIIllIlllllIII+1;end;end);end;return IIlIlIIl(true,{},lIlIlIIIllIIlIIIlIlllIIlI())();end)(string.byte,table.insert,setmetatable);
