[DeepMate_兴趣磁场交互原型.html](https://github.com/user-attachments/files/35455670/DeepMate_.html)
<!doctype html>
<html lang="zh-CN">
<head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>DeepMate 兴趣磁场｜交互原型</title>
<style>
:root{--ink:#202038;--muted:#85849a;--line:#e8e7ef;--paper:#f5f5fa;--purple:#7162db;--purple2:#a495ff;--blue:#6d9bff;--teal:#56dfd1;--pink:#ff86ba;--dark:#14132c;--white:#fff;--shadow:0 14px 38px #20204a0b}
*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--paper);color:var(--ink);font:14px/1.6 -apple-system,BlinkMacSystemFont,"Segoe UI","PingFang SC","Microsoft YaHei",sans-serif}button,input,textarea{font:inherit}button{cursor:pointer}.topbar{height:68px;background:#ffffffed;border-bottom:1px solid var(--line);display:flex;align-items:center;justify-content:space-between;padding:0 max(calc((100vw - 1320px)/2),28px);position:sticky;top:0;z-index:10;backdrop-filter:blur(16px)}.brand{display:flex;align-items:center;gap:10px;font-weight:780;font-size:16px;letter-spacing:.01em}.brand-mark{width:31px;height:31px;border-radius:11px;background:linear-gradient(140deg,#6654d4,#4c85ed);display:grid;place-items:center;color:white;font-weight:800;font-size:15px;box-shadow:0 5px 12px #6757d044}.brand small{font-size:12px;color:#aaa8bc;font-weight:500;margin-left:4px}.top-right{display:flex;align-items:center;gap:18px;color:#6f6e83;font-size:13px}.mini-avatar{width:30px;height:30px;border-radius:50%;background:linear-gradient(135deg,#ffe4b8,#ffacd5);display:grid;place-items:center;color:#603e55;font-weight:700}.shell{max-width:1320px;margin:0 auto;padding:35px 24px 70px}.intro{display:flex;justify-content:space-between;align-items:flex-end;gap:25px;margin-bottom:23px}.eyebrow{color:#7164d6;font-size:11px;font-weight:800;letter-spacing:.15em;text-transform:uppercase}.intro h1{font-size:32px;letter-spacing:-.04em;line-height:1.2;margin:8px 0 8px;color:#211e3a}.intro p{margin:0;color:#77768b;font-size:14px}.intro-note{border:1px solid #e4e1f3;background:#fff;border-radius:14px;padding:11px 15px;color:#6b6781;font-size:12px;max-width:295px}.intro-note b{color:#6252c9}.steps{display:flex;align-items:center;gap:8px;margin:0 0 20px;color:#928fa5;font-size:12px}.step{display:flex;align-items:center;gap:8px}.step-num{width:21px;height:21px;display:grid;place-items:center;background:#e9e7f5;color:#77738c;border-radius:50%;font-size:11px;font-weight:700}.step.current{color:#5646bf;font-weight:700}.step.current .step-num{background:#7162db;color:white}.step-line{width:42px;height:1px;background:#dedce9;margin:0 4px}.workspace{display:grid;grid-template-columns:310px minmax(350px,1fr) 328px;gap:16px;align-items:stretch}.panel{background:#fff;border:1px solid var(--line);border-radius:21px;box-shadow:var(--shadow)}.composer{padding:20px 19px 18px}.panel-head{display:flex;justify-content:space-between;align-items:flex-start;gap:10px;margin-bottom:14px}.panel-head h2{font-size:15px;margin:0;line-height:1.3}.panel-head p{font-size:11px;color:var(--muted);margin:4px 0 0}.counter{font-size:11px;color:#aaa7ba}.label{font-size:11px;color:#747187;font-weight:700;margin:14px 0 8px;display:block}.artifact-modes{display:grid;grid-template-columns:repeat(3,1fr);gap:6px}.mode{border:1px solid var(--line);border-radius:10px;background:#fff;color:#77758a;padding:8px 4px;font-size:11px;transition:.2s}.mode.active{border-color:#a99ef1;color:#5748bf;background:#f4f2ff;box-shadow:0 0 0 2px #f0edff}.mode i{display:block;font-style:normal;font-size:16px;margin-bottom:2px}.artifact{height:138px;border-radius:14px;background:#17172f;position:relative;overflow:hidden;margin-top:9px;color:#fff}.photo-art{position:absolute;inset:0;background:radial-gradient(circle at 24% 72%,#f4a8b5 0,transparent 25%),radial-gradient(circle at 74% 27%,#74d4c4 0,transparent 24%),radial-gradient(circle at 53% 52%,#f0d28c 0,transparent 27%),linear-gradient(135deg,#6256bd,#829fe1 52%,#e8a9bf)}.photo-art:before{content:'';position:absolute;width:92px;height:92px;left:calc(50% - 46px);top:calc(50% - 46px);border-radius:32% 68% 55% 45%;background:linear-gradient(140deg,#fff8,#ffffff19);transform:rotate(28deg);box-shadow:0 10px 40px #25204a55}.photo-art:after{content:'';position:absolute;width:46px;height:46px;left:calc(50% - 23px);top:calc(50% - 23px);border-radius:50%;background:linear-gradient(140deg,#fff9,#ffffff1c);box-shadow:0 0 25px #ffffff44}.artifact-caption{position:absolute;left:13px;bottom:10px;z-index:2}.artifact-caption b{display:block;font-size:12px}.artifact-caption span{font-size:10px;color:#d1d0df}.artifact-tag{position:absolute;right:10px;top:9px;padding:4px 7px;border-radius:7px;background:#ffffff22;backdrop-filter:blur(5px);font-size:9px;color:#fff}.sound-art{display:none;position:absolute;inset:0;background:radial-gradient(ellipse at 50% 100%,#7155dd66,transparent 65%),linear-gradient(135deg,#19182f,#242348)}.wave{height:50px;display:flex;gap:3px;align-items:center;position:absolute;left:12%;right:12%;top:42px;justify-content:center}.wave i{width:3px;border-radius:3px;background:linear-gradient(#73d9e0,#9b7aff);height:var(--h);opacity:.9}.sound-label{position:absolute;left:13px;bottom:11px;font-size:11px;color:#eeedfa}.text-art{display:none;position:absolute;inset:0;background:linear-gradient(135deg,#eeeaff,#dfe7ff);color:#554c8e;padding:22px;font-size:17px;font-family:Georgia,"Songti SC",serif}.text-art small{display:block;font:10px sans-serif;color:#8882a8;margin-top:12px}.upload{position:absolute;right:10px;bottom:10px;z-index:3;border:1px solid #ffffff77;background:#ffffff1d;color:white;border-radius:8px;padding:5px 8px;font-size:10px;backdrop-filter:blur(6px)}.field-label{width:100%;margin-top:10px;border:1px solid var(--line);border-radius:12px;padding:10px 11px;color:#333148;font-size:12px;outline:none;resize:none;height:66px;line-height:1.55}.field-label:focus{border-color:#a89df0;box-shadow:0 0 0 3px #efedff}.helper{font-size:10px;color:#a09eb0;margin:5px 0 0}.scope-row{display:flex;gap:7px}.scope{flex:1;border:1px solid var(--line);background:#fff;color:#77758a;border-radius:9px;padding:7px 8px;font-size:11px}.scope.active{color:#5b4bc5;border-color:#b8aff5;background:#f6f4ff}.privacy{display:flex;gap:8px;align-items:flex-start;color:#77758a;font-size:10px;margin:12px 0 14px;line-height:1.5}.privacy input{accent-color:#7162db;margin:2px 0 0}.publish{width:100%;border:0;border-radius:12px;background:linear-gradient(100deg,#7562dc,#527fe6);color:white;padding:11px 12px;font-weight:700;font-size:12px;box-shadow:0 8px 18px #6b5fd833;transition:transform .2s,box-shadow .2s}.publish:hover{transform:translateY(-1px);box-shadow:0 11px 22px #6b5fd844}.publish.done{background:#1eaa8b}.composer-state{min-height:18px;font-size:10px;color:#9996aa;text-align:center;margin:8px 0 0}.field-panel{padding:17px;position:relative;overflow:hidden;min-height:572px;background:#17162f;border:1px solid #2d2a50;box-shadow:0 20px 50px #1b18351a}.field-head{position:relative;z-index:2;display:flex;justify-content:space-between;align-items:flex-start;color:white}.field-head h2{margin:0;font-size:14px}.field-head p{font-size:10px;color:#aaa8c5;margin:4px 0 0}.live{display:flex;align-items:center;gap:6px;font-size:10px;color:#a8a5c0;border:1px solid #454267;border-radius:50px;padding:4px 8px}.live-dot{width:6px;height:6px;background:#5ed7c5;border-radius:50%;box-shadow:0 0 9px #5ed7c5}.magnetic-field{position:relative;height:410px;margin:13px -4px 0;overflow:hidden;border-radius:16px;background:radial-gradient(ellipse at 50% 52%,#43388255 0%,#2826504a 34%,#17162f 72%)}.magnetic-field:before,.magnetic-field:after{content:"";position:absolute;inset:6% 9%;border:1px solid #ffffff12;border-radius:50%;transform:rotate(-23deg) scaleY(.56);transition:.7s}.magnetic-field:after{inset:16% 17%;border-color:#b9a7ff20;transform:rotate(30deg) scaleY(.54)}.field-active .magnetic-field:before{inset:0 3%;border-color:#70daf333;transform:rotate(-20deg) scaleY(.68);box-shadow:0 0 48px #7667da1b}.field-active .magnetic-field:after{inset:12% 12%;border-color:#d6a0ff3a;transform:rotate(28deg) scaleY(.62)}.field-lines{position:absolute;inset:0;background:radial-gradient(ellipse at 50% 50%,transparent 20%,#a18bff08 45%,transparent 68%);opacity:.9}.core{position:absolute;z-index:3;left:50%;top:50%;transform:translate(-50%,-50%);width:178px;height:178px;border-radius:50%;display:grid;place-items:center;text-align:center;background:radial-gradient(circle at 50% 48%,#423d73 0,#28264c 45%,#201f3d 68%,transparent 70%);transition:.7s}.core:before,.core:after{content:"";position:absolute;border-radius:50%;inset:5px;border:1px solid #a593ff3c;box-shadow:0 0 28px #856ee633,inset 0 0 22px #5d4fc51a}.core:after{inset:16px;border-color:#69dcd249;border-style:dashed;transform:rotate(-18deg)}.field-active .core{filter:drop-shadow(0 0 30px #8a70ff5a);transform:translate(-50%,-50%) scale(1.04)}.magnet-icon{position:relative;width:36px;height:34px;margin:0 auto 6px}.magnet-icon:before{content:"";position:absolute;left:4px;top:3px;width:25px;height:23px;border:7px solid #a994ff;border-bottom:0;border-radius:18px 18px 0 0;filter:drop-shadow(0 0 7px #a58aff88)}.magnet-icon:after{content:"";position:absolute;left:4px;top:21px;width:7px;height:8px;background:#55dcca;border-radius:2px 2px 0 0;box-shadow:18px 0 #ff91c0}.core-title{color:#fff;font-weight:750;font-size:12px}.core-sub{font-size:9px;color:#bcb9d5;margin-top:2px}.core-text{max-width:138px;color:#e7e4ff;font-size:10px;margin-top:6px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.orbit{position:absolute;z-index:2;left:50%;top:50%;width:290px;height:290px;transform:translate(-50%,-50%);border:1px solid #ffffff0b;border-radius:50%;transition:.6s}.field-active .orbit{border-color:#c6bcff24;transform:translate(-50%,-50%) scale(1.08)}.orbit-node{position:absolute;width:60px;height:60px;border-radius:50%;border:1px solid #ffffff27;background:#23213f;color:#d5d3e9;display:grid;place-items:center;text-align:center;font-size:9px;line-height:1.2;box-shadow:0 5px 20px #06061066;opacity:.26;transform:scale(.82);transition:.7s;cursor:pointer}.orbit-node span{font-size:16px;display:block;margin-bottom:1px}.field-active .orbit-node{opacity:1;transform:scale(1);animation:breathe 3s ease-in-out infinite}@keyframes breathe{0%,100%{box-shadow:0 5px 20px #06061066}50%{box-shadow:0 0 24px #8b79ff55}}
.particle{position:absolute;width:5px;height:5px;border-radius:50%;background:#a899ff;opacity:.7;box-shadow:0 0 9px #9c8bff}.p1{left:21%;top:25%}.p2{left:75%;top:23%;background:#61dace}.p3{left:25%;top:76%;background:#ff8ab9}.p4{left:76%;top:72%;background:#8cb5ff}.field-foot{display:flex;justify-content:space-between;align-items:center;color:#aaa7c4;font-size:10px;padding:0 5px}.field-foot b{color:#e8e5ff;font-weight:600}.field-foot .field-action{border:0;background:transparent;color:#a9a4c8;font-size:10px;padding:4px}.field-action:hover{color:white}.attracted{padding:19px 18px 17px;min-height:572px;display:flex;flex-direction:column}.attracted h2{font-size:15px;margin:0}.attracted-head{display:flex;justify-content:space-between;align-items:center}.attracted-head span{font-size:10px;color:#aaa7b8}.attracted-intro{font-size:11px;color:#8b899e;margin:5px 0 12px}.empty-state{flex:1;min-height:300px;border:1px dashed #dedce9;border-radius:15px;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;padding:22px;color:#9794a9;background:#fbfbfd}.empty-icon{width:48px;height:48px;border-radius:16px;background:#f0eff9;display:grid;place-items:center;font-size:21px;color:#7b6cdd;margin-bottom:11px}.empty-state b{font-size:12px;color:#5c5971;margin-bottom:4px}.empty-state p{font-size:10px;max-width:190px;margin:0;line-height:1.6}.spark-list{display:none;flex-direction:column;gap:9px}.field-active .spark-list{display:flex}.field-active .empty-state{display:none}.spark-card{width:100%;text-align:left;background:#fff;border:1px solid #eceaf2;border-radius:14px;padding:12px;transition:.2s;color:var(--ink)}.spark-card:hover,.spark-card.selected{border-color:#b7acf1;background:#faf9ff;transform:translateY(-1px);box-shadow:0 8px 20px #5345ae10}.spark-top{display:flex;align-items:center;gap:8px;margin-bottom:7px}.spark-avatar{width:28px;height:28px;border-radius:10px;display:grid;place-items:center;color:#fff;font-size:12px;background:linear-gradient(135deg,#8171e3,#7ac6da)}.spark-card:nth-child(2) .spark-avatar{background:linear-gradient(135deg,#ed8caf,#aa85e8)}.spark-card:nth-child(3) .spark-avatar{background:linear-gradient(135deg,#5bbab6,#7795e7)}.spark-name{font-size:10px;font-weight:700}.spark-meta{font-size:9px;color:#a3a0b0;margin-left:auto}.spark-card p{margin:0;color:#5f5d73;font-size:11px;line-height:1.5}.spark-tags{display:flex;gap:5px;margin-top:8px}.spark-tags span{font-size:9px;background:#f1effb;color:#69628e;padding:3px 7px;border-radius:99px}.privacy-foot{margin-top:auto;border-top:1px solid #efedf4;padding-top:12px;display:flex;align-items:flex-start;gap:8px;color:#918ea1;font-size:10px;line-height:1.5}.privacy-foot i{font-style:normal;color:#55a18f;font-size:13px}.match-detail{display:none;margin-top:12px;padding:13px;border-radius:14px;background:linear-gradient(140deg,#f5f2ff,#f3f8ff);border:1px solid #e8e4f8}.match-detail.show{display:block;animation:fadein .25s ease}.detail-top{display:flex;justify-content:space-between;align-items:flex-start}.detail-top b{font-size:11px;color:#453d77}.detail-top button{border:0;background:none;color:#8f8ba2;font-size:15px;padding:0}.detail-line{font-size:10px;color:#69677c;margin:8px 0;line-height:1.55}.detail-line strong{color:#5649b5}.activity-options{display:grid;gap:6px;margin:9px 0}.activity-option{border:1px solid #e5e1f2;background:#fff;border-radius:9px;padding:8px 9px;text-align:left;font-size:10px;color:#615e76;transition:.2s}.activity-option.active{border-color:#8878e1;color:#5648bb;background:#f7f5ff}.activity-option span{display:block;font-size:9px;color:#9a97aa;margin-top:2px}.invite{width:100%;border:0;border-radius:10px;background:#6555c9;color:white;padding:9px;font-size:10px;font-weight:700}.invite:hover{background:#5747bb}.invite:disabled{background:#adb9be;cursor:default}.status-note{font-size:9px;color:#8e8aa0;text-align:center;margin:8px 0 0;min-height:14px}.toast{position:fixed;left:50%;bottom:24px;transform:translate(-50%,15px);opacity:0;pointer-events:none;z-index:30;background:#24213e;color:white;border:1px solid #504875;border-radius:12px;padding:11px 16px;font-size:12px;box-shadow:0 15px 35px #12112855;transition:.25s}.toast.show{opacity:1;transform:translate(-50%,0)}.modal-backdrop{position:fixed;inset:0;z-index:20;background:#15132dcc;display:none;align-items:center;justify-content:center;padding:20px;backdrop-filter:blur(5px)}.modal-backdrop.show{display:flex}.modal{width:min(460px,100%);background:#fff;border-radius:23px;padding:25px;box-shadow:0 30px 90px #08071877;animation:fadein .2s ease}.modal-close{float:right;border:0;background:#f3f2f8;color:#77758a;border-radius:50%;width:29px;height:29px;font-size:17px}.modal h2{font-size:20px;margin:5px 0 5px}.modal-sub{font-size:12px;color:#858298;margin:0 0 18px}.exchange{display:grid;grid-template-columns:1fr 32px 1fr;align-items:center;gap:6px;margin:16px 0}.exchange-card{background:#f7f6fb;border:1px solid #eceaf3;border-radius:14px;padding:13px;text-align:center;min-height:105px}.exchange-card .emoji{font-size:24px;display:block;margin-bottom:7px}.exchange-card b{font-size:10px;display:block}.exchange-card span{font-size:9px;color:#8f8b9e}.exchange-arrow{text-align:center;color:#8c7be1;font-size:18px}.modal-input{width:100%;border:1px solid #e5e3ed;border-radius:11px;padding:10px 12px;resize:vertical;min-height:68px;font-size:11px;outline:none}.modal-input:focus{border-color:#998ce5}.modal-actions{display:flex;justify-content:flex-end;gap:8px;margin-top:15px}.btn-secondary,.btn-primary{border-radius:10px;padding:9px 14px;font-size:11px}.btn-secondary{border:1px solid #e4e2eb;background:white;color:#77758a}.btn-primary{border:0;background:#6656c7;color:white;font-weight:700}.footer-note{text-align:center;color:#a4a1b1;font-size:10px;margin-top:20px}
@keyframes fadein{from{opacity:0;transform:translateY(5px)}to{opacity:1;transform:translateY(0)}}
@media(max-width:1100px){.workspace{grid-template-columns:290px minmax(350px,1fr)}.attracted{grid-column:1/-1;min-height:0}.spark-list{display:none;grid-template-columns:repeat(3,1fr)}.field-active .spark-list{display:grid}.empty-state{min-height:170px}.privacy-foot{margin-top:15px}}
@media(max-width:760px){.topbar{height:58px;padding:0 15px}.top-right>span{display:none}.shell{padding:23px 13px 42px}.intro{display:block}.intro h1{font-size:27px}.intro-note{margin-top:14px;max-width:none}.steps{overflow-x:auto;white-space:nowrap;padding-bottom:3px}.step-line{width:20px;flex:none}.workspace{grid-template-columns:1fr}.field-panel{grid-row:1;min-height:0}.magnetic-field{height:330px}.orbit{width:245px;height:245px}.core{width:155px;height:155px}.composer{grid-row:2}.attracted{grid-column:auto;grid-row:3}.spark-list{grid-template-columns:1fr}.empty-state{min-height:155px}.attracted{min-height:0}.privacy-foot{margin-top:15px}}
@media(prefers-reduced-motion:reduce){*,*:before,*:after{animation-duration:.01ms!important;scroll-behavior:auto!important;transition-duration:.01ms!important}}
</style>
<style>
.interest-box{border:1px solid #e9e6f1;border-radius:13px;background:#fbfaff;padding:11px;margin:12px 0 13px}.interest-box-head{display:flex;justify-content:space-between;gap:8px;align-items:baseline}.interest-box-head b{font-size:11px;color:#403b56}.interest-box-head span{font-size:9px;color:#9692a5}.interest-input{display:flex;gap:6px;margin:9px 0}.interest-input input{width:100%;min-width:0;border:1px solid #e4e1ec;border-radius:9px;padding:8px 9px;font-size:10px;outline:none}.interest-input input:focus{border-color:#a99ef1;box-shadow:0 0 0 2px #f0edff}.interest-input button{flex:none;border:0;border-radius:9px;padding:7px 10px;background:#eeeaff;color:#5b4bc5;font-size:10px;font-weight:700}.interest-chips{display:flex;flex-wrap:wrap;gap:5px}.interest-chip{border:1px solid #e5e1ee;background:white;color:#6d6980;border-radius:999px;padding:5px 8px;font-size:9px;line-height:1.2}.interest-chip:hover,.interest-chip.selected{border-color:#9d8de7;background:#f4f1ff;color:#5647bb}.interest-chip.selected:before{content:"✓ ";font-weight:800}.selected-interests{display:flex;flex-wrap:wrap;gap:5px;margin-top:9px;min-height:20px}.selected-interest{border-radius:999px;background:#eeeaff;color:#5647bb;padding:4px 7px;font-size:9px;display:inline-flex;align-items:center;gap:5px}.selected-interest button{border:0;background:transparent;color:#6e61b6;padding:0;font-size:12px;line-height:1}.interest-hint{font-size:9px;color:#9692a5;margin:7px 0 0}
.orbit{inset:0;left:0;top:0;width:100%;height:100%;transform:none;border:0;border-radius:0;transition:none}.field-active .orbit{transform:none;border:0}.orbit-node{left:50%;top:50%;right:auto;bottom:auto;margin:0;opacity:.92;transform:translate(-50%,-50%);cursor:default}.field-active .orbit-node{opacity:1;transform:translate(-50%,-50%)}
.orbit-node .orbit-label{font-size:9px;display:block;max-width:54px;margin:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
[hidden]{display:none!important}
#fieldPanel,#matchDetail{scroll-margin-top:76px}
.approach-layer{position:absolute;inset:0;z-index:4;pointer-events:none}
.approach-person{--visitor:#62edd9;position:absolute;left:var(--end-x);top:var(--end-y);width:48px;height:48px;display:grid;place-items:center;transform:translate(-50%,-50%);border-radius:50%;border:1px solid var(--visitor);background:#1e3650;color:white;font-size:22px;box-shadow:0 0 24px #61f5d474,inset 0 0 12px #62edd93a}
.approach-person:disabled{cursor:default}
.approach-person:not(:disabled){pointer-events:auto}
.approach-person:not(:disabled):after{content:"";position:absolute;inset:-7px;border:1px solid #62edd94a;border-radius:50%;animation:arrival-ring 1.1s ease-out 2}
.approach-person:focus-visible{outline:2px solid white;outline-offset:4px}
.approach-person.is-moving{animation:visitor-travel 2.2s both}
.approach-trace{position:absolute;width:var(--trace-width);left:var(--target-x);top:var(--target-y);transform:rotate(var(--trace-angle));transform-origin:0 50%;border-top:1px dashed #7aefdfb0;opacity:0;transition:opacity .45s;z-index:-1}
.approach-layer.has-arrived .approach-trace{opacity:1}
.field-active .orbit-node.is-resonating{border-color:#6cf1dc!important;background:#233e50;color:#d4fff8;animation:resonate 1.4s ease-in-out infinite}
@keyframes resonate{0%,100%{box-shadow:0 0 12px #62edd94d}50%{box-shadow:0 0 26px #62edd9a6}}
@keyframes arrival-ring{from{transform:scale(.82);opacity:1}to{transform:scale(1.65);opacity:0}}
@keyframes visitor-travel{
  0%{left:var(--start-x);top:var(--start-y);opacity:0;transform:translate(-50%,-50%) scale(.24)}
  24%{left:var(--outer-x);top:var(--outer-y);opacity:.75;transform:translate(-50%,-50%) scale(.52)}
  66%{left:var(--inner-x);top:var(--inner-y);opacity:1;transform:translate(-50%,-50%) scale(.8);animation-timing-function:ease-out}
  100%{left:var(--end-x);top:var(--end-y);transform:translate(-50%,-50%) scale(1)}
}
.approach-status{display:grid;grid-template-columns:auto minmax(0,1fr);align-items:center;gap:10px;margin:8px 0 12px;padding:11px 12px;border:1px solid #555280;border-radius:13px;background:#211f3d;color:#efedff}
.approach-signal{width:8px;height:8px;border-radius:50%;background:#67e6d4;box-shadow:0 0 13px #67e6d480}
.approach-status b,.approach-status small{display:block;overflow-wrap:anywhere}
.approach-status b{font-size:12px}
.approach-status small{color:#b8b5d2;font-size:10px}
.approach-actions{grid-column:2;display:flex;flex-wrap:wrap;gap:7px}
.approach-actions button{border:1px solid #5a557f;border-radius:8px;background:transparent;color:#ddd9f8;padding:5px 8px;font-size:10px}
.approach-actions button:first-child{color:#bafbeb;background:#2b4b53;border-color:#507b7c}
.spark-list.has-visitors{display:flex;margin-bottom:12px}
.spark-card{animation:fadein .3s ease}
.spark-tags{flex-wrap:wrap;overflow-wrap:anywhere}
.approach-person:not(:disabled):hover,.approach-actions button:hover{filter:brightness(1.18)}
@media(min-width:761px) and (max-width:1100px){.spark-list.has-visitors{display:grid}}
.approach-person.is-moving{background:#2c5b62;box-shadow:0 0 12px 3px #70ffe4a1,0 0 36px #73ffda91}
.approach-person.is-moving:before{content:"";position:absolute;right:75%;top:50%;width:70px;height:3px;background:linear-gradient(90deg,transparent,#6efce0aa);transform-origin:right;transform:rotate(var(--tail-angle));border-radius:99px}
.challenge-board{margin-top:13px;padding-top:12px;border-top:1px solid #dcd8ee;color:#30294e}
.challenge-head,.challenge-controls{display:flex;align-items:center;justify-content:space-between;gap:8px}
.challenge-head h3{margin:0;font-size:14px;color:#342a67}
.challenge-head span{font-size:10px;padding:2px 7px;border-radius:20px;background:#e6e2fb;color:#51439c;white-space:nowrap}
.challenge-prompt{margin:8px 0 4px;font-size:12px;font-weight:650;line-height:1.6;overflow-wrap:anywhere}
.challenge-status{font-size:11px;line-height:1.6;color:#625b79;margin:4px 0 10px}
.challenge-actions,.challenge-controls{display:flex;flex-wrap:wrap;gap:7px;margin-bottom:4px}
.challenge-envelopes,.challenge-results{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:7px;margin:10px 0}
.challenge-envelopes>div,.challenge-results article{padding:9px;border:1px solid #dfdae9;border-radius:10px;background:#fff;overflow-wrap:anywhere}
.challenge-envelopes b,.challenge-envelopes span{display:block;font-size:10px}
.challenge-envelopes span{color:#685e84;margin-top:3px}
.challenge-board label{display:block;font-size:11px;font-weight:650;margin:9px 0 5px}
.challenge-controls small{font-size:10px;color:#685e84}
.challenge-board .btn-primary:disabled{background:#e1ddef;color:#665c80;cursor:default}
.challenge-results{grid-template-columns:minmax(0,1fr)}
.challenge-results h4{font-size:11px;margin:0 0 4px;color:#4e408d}
.challenge-results p{font-size:12px;margin:0;white-space:pre-wrap}
.challenge-results button{justify-self:start}
.challenge-note{margin:0 0 10px;padding:8px 9px;border-radius:8px;background:#fff9;color:#5d5574;font-size:11px;white-space:pre-wrap;overflow-wrap:anywhere}
.recipient-preview{margin:8px 0 12px;padding:10px;border:1px solid #ddd7ee;border-radius:11px;background:#fff;overflow-wrap:anywhere}
.recipient-preview h4{margin:0;font-size:11px;color:#4e408d}
.recipient-preview p{margin:6px 0 9px;font-size:11px}
.challenge-views{display:flex;flex-wrap:wrap;gap:5px;align-items:center;margin:9px 0;padding:5px;background:#eae6f8;border-radius:9px}
.challenge-views>span{font-size:10px;color:#605483;padding:0 4px}
.challenge-views button{border:1px solid transparent;border-radius:7px;padding:5px 8px;background:transparent;font-size:11px;color:#55487c}
.challenge-views button[aria-pressed="true"]{background:#fff;border-color:#d8cee9;color:#3f3075;font-weight:700}
.challenge-followup article h5{margin:0 0 4px;font-size:10px;color:#58479a}
.challenge-followup{padding-top:9px;border-top:1px solid #e1dcee}
.challenge-followup h4{font-size:12px}
.challenge-followup .btn-primary{margin-top:6px}
.challenge-followup article{margin-top:7px}
.challenge-followup p{color:#50476c}
</style>
</head>
<body>
<header class="topbar">
  <div class="brand"><div class="brand-mark">D</div><div>DeepMate <small>兴趣磁场</small></div></div>
  <div class="top-right"><span>发现</span><span>社区</span><span>我的磁场</span><div class="mini-avatar">知</div></div>
</header>
<main class="shell">
  <section class="intro">
    <div><div class="eyebrow">INTEREST SKILL · SOCIAL DISCOVERY</div><h1>把喜欢的事，放进兴趣磁场</h1><p>先选几个兴趣磁石，再分享一件作品或经历，看看谁带着自己的兴趣靠近。</p></div>
    <div class="intro-note"><b>交互原型</b> · 示例内容仅用于展示。公开的是你确认过的兴趣卡，不是聊天记录或个人记忆。</div>
  </section>
  <div class="steps" aria-label="交互步骤">
    <div class="step current" id="step1"><span class="step-num">1</span><span>放入兴趣磁石</span></div><span class="step-line"></span>
    <div class="step" id="step2"><span class="step-num">2</span><span>看看谁靠近</span></div><span class="step-line"></span>
    <div class="step" id="step3"><span class="step-num">3</span><span>一起做点什么</span></div>
  </div>
  <section class="workspace">
    <aside class="panel composer">
      <div class="panel-head"><div><h2>先放几枚兴趣磁石</h2><p>选几个现在想遇见同好的兴趣</p></div><span class="counter">随时可加</span></div>
      <div class="interest-box"><div class="interest-box-head"><b>你的兴趣</b><span id="interestCount">还没选</span></div><div class="interest-input"><input id="interestInput" maxlength="20" placeholder="自己写一个兴趣"><button type="button" id="addInterest">添加</button></div><div class="interest-chips" id="interestChoices"></div><button class="quiet" type="button" id="moreInterests" style="border:0;background:transparent;color:#7770a0;font-size:9px;padding:7px 1px 0">看看更多兴趣 ↓</button><div class="selected-interests" id="selectedInterests"></div><p class="interest-hint">不用把所有爱好一次选完。先选 3–5 个，也可以只选 1 个；想到其他兴趣再补充。</p></div>
      <span class="label">选一段和兴趣有关的内容放进磁场</span>
      <div class="artifact-modes">
        <button class="mode active" data-mode="photo"><i>▧</i>一张作品</button>
        <button class="mode" data-mode="sound"><i>♫</i>一段声音</button>
        <button class="mode" data-mode="note"><i>✎</i>一段文字</button>
      </div>
      <div class="artifact" id="artifact">
        <div class="photo-art" id="photoArt"></div>
        <div class="sound-art" id="soundArt"><div class="wave" id="wave"></div><div class="sound-label">我的声音片段</div></div>
        <div class="text-art" id="textArt">把你喜欢的事，放进磁场里。<small>一段兴趣片段</small></div>
        <div class="artifact-tag" id="artifactTag">作品片段 · 示例</div>
        <div class="artifact-caption"><b id="artifactTitle">我的兴趣作品</b><span id="artifactSub">选择一件你愿意分享的内容</span></div>
        <button class="upload" id="uploadBtn">＋ 换成我的内容</button>
        <input id="fileInput" type="file" accept="image/*" hidden>
      </div>
      <label class="label" for="interestText">愿意分享的话，写一句你的感受</label>
      <textarea class="field-label" id="interestText" maxlength="100" placeholder="比如：我喜欢【兴趣】里的【某个细节】，也想听听别人怎么体验"></textarea>
      <p class="helper">可以分享作品、声音或文字。兴趣可以先多选，分享内容再挑一件就好。</p>
      <span class="label">想遇见谁？</span>
      <div class="scope-row"><button class="scope active" data-scope="online">线上同好</button><button class="scope" data-scope="nearby">同城兴趣</button></div>
      <label class="privacy"><input id="privacyCheck" type="checkbox" checked><span>只公开这张兴趣卡。聊天记录、记忆和其他资料不会跟着分享。</span></label>
      <button class="publish" id="publishBtn">放进磁场 <span>↗</span></button>
      <p class="composer-state" id="composerState">你可以先预览；确认后才会出现在磁场里。</p>
    </aside>

    <section class="panel field-panel" id="fieldPanel">
      <div class="field-head"><div><h2>你的兴趣磁场</h2><p id="fieldStatus">还没有发布 · 你可以先调整这张卡</p></div><div class="live"><span class="live-dot"></span><span id="liveLabel">预览中</span></div></div>
      <div class="magnetic-field" id="magneticField">
        <div class="field-lines"></div><span class="particle p1"></span><span class="particle p2"></span><span class="particle p3"></span><span class="particle p4"></span>
        <div class="orbit" id="orbit" aria-hidden="true"></div>
        <div class="approach-layer" id="approachLayer" hidden>
          <div class="approach-trace" aria-hidden="true"></div>
          <button type="button" class="approach-person" id="approachPerson" aria-controls="matchDetail" disabled>✦</button>
        </div>
        <div class="core"><div><div class="magnet-icon"></div><div class="core-title">你的兴趣磁石</div><div class="core-sub">最近着迷于</div><div class="core-text" id="coreText">先从左侧放入兴趣</div></div></div>
      </div>
      <div class="approach-status" id="approachStatus" hidden>
        <span class="approach-signal" aria-hidden="true"></span>
        <div role="status"><b id="approachTitle"></b><small id="approachCopy"></small></div>
        <div class="approach-actions">
          <button type="button" id="viewVisitor" aria-controls="matchDetail" hidden>看 TA 的片段 ↗</button>
          <button type="button" id="nextVisitor" hidden>看看还有谁</button>
        </div>
      </div>
      <div class="field-foot"><span><b id="fieldCount">0</b> 枚兴趣磁石已放入</span><button class="field-action" id="retractBtn">收回磁石</button></div>
    </section>

    <aside class="panel attracted">
      <div class="attracted-head"><h2>靠近的兴趣碎片</h2><span id="sparkCount">等待发布</span></div>
      <p class="attracted-intro">先看对方分享的东西，再决定要不要认识。</p>
      <div class="empty-state" id="emptyState"><div class="empty-icon">✧</div><b>这里还没有人靠近</b><p>发布兴趣卡后，相关的作品和经历会慢慢出现在这里。</p></div>
      <div class="spark-list" id="sparkList"></div>
      <template id="sparkTemplate">
        <button type="button" class="spark-card" aria-controls="matchDetail" aria-expanded="false">
          <div class="spark-top"><span class="spark-avatar" aria-hidden="true"></span><span class="spark-name"></span><span class="spark-meta">已靠近</span></div>
          <p></p><div class="spark-tags"><span></span></div>
        </button>
      </template>
      <div class="match-detail" id="matchDetail">
        <div class="detail-top"><b id="detailTitle" tabindex="-1">你们为什么会互相吸引</b><button id="closeDetail" aria-label="关闭">×</button></div>
        <div class="detail-line" id="detailCopy"></div>
        <div class="activity-options" id="activityOptions">
          <button class="activity-option active" data-action="exchange">交换一件兴趣作品<span>先交换作品，不必立刻聊天</span></button>
          <button class="activity-option" data-action="challenge">一起完成一个小挑战<span>各做同一道小题，提交后互看两份发现</span></button>
        </div>
        <button class="invite" id="inviteBtn">发出邀请</button>
        <p class="status-note" id="statusNote">对方同意后，才会开始交换。</p>
        <section class="challenge-board" id="challengeBoard" aria-labelledby="challengeTitle" hidden>
          <div class="challenge-head"><h3 id="challengeTitle" tabindex="-1">双人小挑战</h3><span id="challengeBadge"></span></div>
          <div class="challenge-views" role="group" aria-label="切换挑战视角">
            <span>双视角演示</span>
            <button type="button" id="senderView" aria-pressed="true">发起人</button>
            <button type="button" id="recipientView" aria-pressed="false">收件人</button>
          </div>
          <p id="challengePrompt" class="challenge-prompt"></p>
          <p id="challengeStatus" class="challenge-status" role="status"></p>
          <p id="challengeInviteNote" class="challenge-note" hidden></p>
          <div class="challenge-actions" id="challengePending" hidden>
            <button class="btn-primary" id="viewRecipient" type="button" aria-controls="recipientPreview">切到收件人视角</button>
            <button class="btn-secondary" id="withdrawChallenge" type="button">撤回邀请</button>
          </div>
          <section class="recipient-preview" id="recipientPreview" aria-labelledby="recipientHeading" hidden>
            <h4 id="recipientHeading" tabindex="-1"></h4><p id="recipientTopic"></p><p id="recipientInviteCopy"></p>
            <div class="challenge-actions">
              <button class="btn-primary" type="button" id="acceptChallenge">接受挑战</button>
              <button class="btn-secondary" type="button" id="declineChallenge">暂不参加</button>
            </div>
          </section>
          <div class="challenge-envelopes" id="challengeEnvelopes" hidden>
            <div><b>你的发现</b><span id="yourEnvelope"></span></div>
            <div><b id="theirEnvelopeTitle"></b><span id="theirEnvelope"></span></div>
          </div>
          <form id="challengeForm" hidden>
            <label for="challengeDraft">写下你的发现</label>
            <textarea class="modal-input" id="challengeDraft" maxlength="200" required rows="3" placeholder="一个你注意到的细节，或者一次让你意外的尝试"></textarea>
            <div class="challenge-controls"><small id="challengeLength">0 / 200</small><button class="btn-primary" id="submitChallenge" type="submit" disabled>提交并同意互看</button></div>
          </form>
          <div class="challenge-results" id="challengeResults" hidden>
            <article><h4>你的发现</h4><p id="yourDiscovery"></p></article>
            <article><h4 id="theirDiscoveryTitle"></h4><p id="theirDiscovery"></p></article>
            <div class="challenge-followup">
              <h4>想接着聊这个发现吗？</h4>
              <div id="followupThread" aria-label="挑战里的对话" aria-live="polite" hidden></div>
              <button class="btn-primary" type="button" id="openFollowup" aria-controls="followupForm" hidden>问 TA 一个问题</button>
              <form id="followupForm" hidden>
                <label for="followupDraft">接着对方的发现说</label>
                <textarea class="modal-input" id="followupDraft" maxlength="160" required rows="2"></textarea>
                <div class="challenge-actions">
                  <button class="btn-primary" type="submit" id="sendFollowup">发送问题</button>
                  <button class="btn-secondary" type="button" id="cancelFollowup">先不聊</button>
                </div>
              </form>
            </div>
          </div>
          <button class="btn-secondary" id="backToField" type="button" hidden>回到磁场</button>
        </section>
      </div>
      <div class="privacy-foot"><i>◈</i><span>互相愿意才连接。对方还没同意前，你的身份和联系方式不会展示。</span></div>
    </aside>
  </section>
  <p class="footer-note">兴趣先靠近，人再决定要不要认识。同好为演示角色。切换视角可以亲手完成双方的操作。</p>
</main>
<div class="toast" id="toast"></div>
<div class="modal-backdrop" id="modalBackdrop" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
  <div class="modal"><button class="modal-close" id="modalClose">×</button><div class="eyebrow">A SMALL SHARED ACTIVITY</div><h2 id="modalTitle">发起一次兴趣交换</h2><p class="modal-sub" id="modalSub">先交换一件和兴趣有关的东西，不需要马上开始聊天。</p>
    <div class="exchange"><div class="exchange-card"><span class="emoji" id="yourEmoji">✦</span><b>你分享</b><span id="yourShare">一件兴趣作品</span></div><div class="exchange-arrow">⇄</div><div class="exchange-card"><span class="emoji" id="theirEmoji">🎧</span><b>对方分享</b><span id="theirShare">一件同好作品</span></div></div>
    <textarea class="modal-input" id="inviteText" aria-label="邀请留言" maxlength="200">想交换一件和兴趣有关的作品吗？</textarea>
    <div class="modal-actions"><button class="btn-secondary" id="cancelInvite">再想想</button><button class="btn-primary" id="sendInvite">发出邀请</button></div>
  </div>
</div>
<script>
const $=(id)=>document.getElementById(id);
const modeButtons=[...document.querySelectorAll('.mode')];
const starterInterests=['读书','看电影','做饭','听音乐','游戏','摄影','跑步','旅行','养宠物','手作'];
const moreInterestGroups={'文化娱乐':['看展','追剧','漫画','桌游','播客','独立音乐','现场演出'],'运动户外':['骑行','徒步','露营','攀岩','羽毛球','游泳','滑板'],'生活日常':['咖啡','烘焙','植物','逛市集','城市散步','穿搭','探店'],'创作表达':['写作','画画','拍视频','设计','跳舞','做模型','收藏']};
let selectedInterests=[],showMoreInterests=false;
const interestScenes = new Map([
  ['读书', ['纸页', '📖', '一条读书摘录', '读到喜欢的句子，我会想它和自己的生活有什么关系。']],
  ['摄影', ['柚子', '📷', '一张傍晚的照片', '下班路上同一条街，只有这十分钟的光让我想停下来。']],
  ['听音乐', ['眠耳', '🎧', '一段循环播放的前奏', '有首歌最近听了太多遍，但每次听到前奏还是会停一下。']],
  ['看电影', ['三帧', '🎬', '一段观影笔记', '有场戏的对白很少，走出影院反而一直在想。']],
  ['做饭', ['山栗', '🥐', '一份厨房记录', '同一个配方试了三次，终于找到自己喜欢的口感。']],
  ['烘焙', ['米粒', '🥐', '一份烘焙记录', '把面团放过夜，第二天烤出来的边缘比想象中更脆。']],
  ['桌游', ['松饼', '🎲', '一场桌游记录', '第一次玩合作桌游，没想到大家能用完全不同的思路解同一关。']],
  ['植物', ['小枝', '🌱', '一张新叶照片', '等了快一个月，新叶终于展开了，颜色和老叶差很多。']],
  ['骑行', ['小满', '🚲', '一段骑行随记', '今天临时绕了条小路，发现一段很安静的缓坡。']],
  ['跑步', ['慢半拍', '👟', '一次跑步记录', '这次没看配速，反而发现了平时没留意的路边小店。']]
]);
const reducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)');
let activeMode='photo', selectedFragment=null, selectedAction='exchange', published=false, uploadedName='';
let publishedInterests = [], encounters = [], activeEncounter = null, approachTimer;

function toast(msg){const t=$('toast');t.textContent=msg;t.classList.add('show');setTimeout(()=>t.classList.remove('show'),2400)}
function renderInterestChoices(){const root=$('interestChoices');root.replaceChildren();const makeChip=item=>{const b=document.createElement('button');b.type='button';b.className='interest-chip'+(selectedInterests.includes(item)?' selected':'');b.textContent=item;b.addEventListener('click',()=>toggleInterest(item));return b};if(showMoreInterests){for(const [group,items] of Object.entries(moreInterestGroups)){const section=document.createElement('div');section.style.cssText='width:100%';const label=document.createElement('div');label.style.cssText='font-size:9px;color:#9692a5;margin:7px 0 4px';label.textContent=group;const row=document.createElement('div');row.className='interest-chips';items.forEach(item=>row.append(makeChip(item)));section.append(label,row);root.append(section)}}else starterInterests.forEach(item=>root.append(makeChip(item)));$('moreInterests').textContent=showMoreInterests?'收起更多兴趣 ↑':'看看更多兴趣 ↓'}
function renderSelectedInterests(){const root=$('selectedInterests');root.replaceChildren();$('interestCount').textContent=selectedInterests.length?`已选 ${selectedInterests.length} 个`:'还没选';if(!selectedInterests.length){const note=document.createElement('span');note.className='interest-hint';note.textContent='从上面的常见兴趣里挑，或自己写一个';root.append(note)}else{selectedInterests.forEach(item=>{const chip=document.createElement('span');chip.className='selected-interest';const label=document.createElement('span');label.textContent=item;const remove=document.createElement('button');remove.type='button';remove.textContent='×';remove.setAttribute('aria-label','移除 '+item);remove.addEventListener('click',()=>toggleInterest(item));chip.append(label,remove);root.append(chip)})}const orbit=$('orbit'),field=$('magneticField'),fieldWidth=field.clientWidth||460;orbit.replaceChildren();const fieldInterests=published?publishedInterests:selectedInterests;const count=fieldInterests.length,perRing=8,ringCount=Math.ceil(count/perRing),lastRadius=count?126+(ringCount-1)*40:126;const baseHeight=window.innerWidth<=760?330:410;field.style.height=Math.max(baseHeight,Math.ceil((lastRadius+36)*2))+'px';const xScale=Math.min(1,Math.max(.35,(fieldWidth/2-34)/lastRadius));fieldInterests.forEach((item,index)=>{const ring=Math.floor(index/perRing),start=ring*perRing,ringSize=Math.min(perRing,count-start),slot=index-start,angle=-Math.PI/2+(2*Math.PI*slot/ringSize)+(ring%2)*(Math.PI/ringSize),radius=126+ring*40,node=document.createElement('div'),icon=document.createElement('span');node.className='orbit-node';node.setAttribute('aria-label',item+'兴趣点');node.title=item;icon.textContent=['✦','♫','▧','⌖','✧','◉','✳','◇'][index%8];const label=document.createElement('span');label.className='orbit-label';label.textContent=item;node.append(icon,label);node.style.left=`calc(50% + ${Math.cos(angle)*radius*xScale}px)`;node.style.top=`calc(50% + ${Math.sin(angle)*radius}px)`;node.style.borderColor=['#75dae1aa','#b59affaa','#f098c5aa','#78aaffaa'][index%4];node.style.animationDelay=(index*.12)+'s';orbit.append(node)});$('coreText').textContent=count?fieldInterests.slice(0,3).join(' · ')+(count>3?'…':''):'先放入一个兴趣';if(activeEncounter)positionVisitor(activeEncounter);renderInterestChoices()}
function toggleInterest(value){const v=value.trim();if(!v)return;const i=selectedInterests.findIndex(x=>x.toLowerCase()===v.toLowerCase());if(i>=0)selectedInterests.splice(i,1);else selectedInterests.push(v);renderSelectedInterests();
  if (published) {
    const edited = !samePublishedInterests();
    $('publishBtn').textContent = edited ? '更新兴趣磁石 ↗' : '磁场已开启 ✓';
    $('composerState').textContent = edited ? '已调整兴趣，更新后会按新兴趣寻找同好。' : '兴趣磁石已放入磁场；你仍可以修改或收回。';
  }
}
function addInterest(){const input=$('interestInput'),value=input.value.trim();if(!value){input.focus();return}if(selectedInterests.some(x=>x.toLowerCase()===value.toLowerCase())){toast('这个兴趣已经选过了');input.value='';return}toggleInterest(value);input.value='';input.focus()}
renderSelectedInterests();$('addInterest').addEventListener('click',addInterest);$('interestInput').addEventListener('keydown',e=>{if(e.key==='Enter'){e.preventDefault();addInterest()}});$('moreInterests').addEventListener('click',()=>{showMoreInterests=!showMoreInterests;renderInterestChoices()});window.addEventListener('resize',renderSelectedInterests);
function setMode(mode){activeMode=mode;modeButtons.forEach(b=>b.classList.toggle('active',b.dataset.mode===mode));$('photoArt').style.display=mode==='photo'?'block':'none';$('soundArt').style.display=mode==='sound'?'block':'none';$('textArt').style.display=mode==='note'?'block':'none';$('fileInput').accept=mode==='photo'?'image/*':mode==='sound'?'audio/*':'.txt';$('artifactTag').textContent=mode==='photo'?'图片片段':mode==='sound'?'声音片段':'文字片段';$('artifactTitle').textContent=mode==='photo'?'我的兴趣作品':mode==='sound'?'一段声音片段':'一段文字片段';$('artifactSub').textContent='选择一件你愿意分享的内容';$('uploadBtn').textContent=mode==='photo'?'＋ 添加我的照片':mode==='sound'?'＋ 添加我的录音':'＋ 添加我的文字';if(mode==='sound'&&$('wave').children.length===0){for(let i=0;i<42;i++){const bar=document.createElement('i');bar.style.setProperty('--h',(8+Math.random()*36)+'px');$('wave').appendChild(bar)}}}
modeButtons.forEach(b=>b.addEventListener('click',()=>setMode(b.dataset.mode)));
document.querySelectorAll('.scope').forEach(b=>b.addEventListener('click',()=>{document.querySelectorAll('.scope').forEach(x=>x.classList.remove('active'));b.classList.add('active');toast(b.dataset.scope==='nearby'?'磁场范围：同城兴趣':'磁场范围：线上同好')}));
$('uploadBtn').addEventListener('click',()=>$('fileInput').click());
$('fileInput').addEventListener('change',e=>{const f=e.target.files[0];if(!f)return;uploadedName=f.name;$('artifactTitle').textContent=f.name;$('artifactSub').textContent='已加入这张兴趣卡';if(f.type.startsWith('image/')){const reader=new FileReader();reader.onload=()=>{$('photoArt').style.backgroundImage=`linear-gradient(0deg,#101023bd,transparent 70%),url(${reader.result})`;$('photoArt').style.backgroundSize='cover';$('photoArt').style.backgroundPosition='center'};reader.readAsDataURL(f)}else if(f.type.startsWith('audio/')){$('soundArt').querySelector('.sound-label').textContent=f.name}toast('已放入兴趣片段')});
function makeEncounter(interest, index) {
  const scene = interestScenes.get(interest);
  const [alias, emoji, their, quote] = scene || [
    ['拾光', '🌿', '一段兴趣随记', '最近又捡起来玩了。最好玩的反而是那些计划之外的小发现。'],
    ['小岛', '🌙', '一个新发现', '前几天试了个新做法，意外打开了思路，想看看别人是怎么玩的。'],
    ['阿洛', '✦', '一张灵感便签', '这个爱好里有些细节，自己玩久了会格外在意。你也有这种感觉吗？']
  ][index % 3];
  return {interest, index, alias, emoji, their, quote, arrived: false, sent: false, challenge: null, card: null};
}

function addSpark(encounter) {
  const card = $('sparkTemplate').content.firstElementChild.cloneNode(true);
  card.querySelector('.spark-avatar').textContent = encounter.emoji;
  card.querySelector('.spark-name').textContent = encounter.alias + ' · ' + encounter.their;
  card.querySelector('p').textContent = '“' + encounter.quote + '”';
  card.querySelector('.spark-tags span').textContent = encounter.interest;
  card.addEventListener('click', () => showFragment(encounter));
  $('sparkList').append(card);
  encounter.card = card;
  encounter.arrived = true;
  $('sparkList').classList.add('has-visitors');
  $('emptyState').hidden = true;
  $('sparkCount').textContent = encounters.filter(person => person.arrived).length + ' 人已靠近';
}

function positionVisitor(encounter) {
  const layer = $('approachLayer');
  const nodes = [...$('orbit').children];
  const target = nodes[encounter.index];
  if (!target) return;
  $('orbit').querySelector('.is-resonating')?.classList.remove('is-resonating');
  target.classList.add('is-resonating');

  const width = layer.clientWidth;
  const height = layer.clientHeight;
  const x = target.offsetLeft;
  const y = target.offsetTop;
  const side = width - x > x ? 1 : -1;
  const vertical = y > height / 2 ? 1 : -1;
  const candidates = [[74 * side, 0], [58 * side, 50 * vertical], [0, 70 * vertical], [58 * side, -50 * vertical], [-70 * side, 0]];
  const points = candidates.map(([dx, dy]) => [
    Math.max(28, Math.min(width - 28, x + dx)),
    Math.max(28, Math.min(height - 28, y + dy))
  ]);
  // Preserve space around the existing magnets, including when several rings are present.
  const clearance = ([px, py]) => Math.min(...nodes.map(node => Math.hypot(px - node.offsetLeft, py - node.offsetTop)));
  const [endX, endY] = points.reduce((best, point) => clearance(point) > clearance(best) ? point : best);
  const startX = endX > width / 2 ? width + 12 : -12;
  const startY = endY > height / 2 ? height * .88 : height * .12;
  const length = Math.hypot(endX - x, endY - y);
  const positions = {
    'start-x': startX, 'start-y': startY,
    'outer-x': startX * .65 + endX * .35, 'outer-y': startY,
    'inner-x': startX * .22 + endX * .78, 'inner-y': startY * .36 + endY * .64,
    'end-x': endX, 'end-y': endY,
    'target-x': x, 'target-y': y,
    'trace-width': length
  };
  for (const [name, value] of Object.entries(positions)) layer.style.setProperty('--' + name, value + 'px');
  layer.style.setProperty('--tail-angle', (startX > endX ? Math.PI : 0) + 'rad');
  layer.style.setProperty('--trace-angle', Math.atan2(endY - y, endX - x) + 'rad');
}

function approach(encounter) {
  activeEncounter = encounter;
  const layer = $('approachLayer');
  const person = $('approachPerson');
  $('viewVisitor').hidden = true;
  $('nextVisitor').hidden = true;
  $('approachTitle').textContent = '有人被「' + encounter.interest + '」吸引';
  $('approachCopy').textContent = '一个光点正从磁场边缘靠近。';
  $('fieldStatus').textContent = '你的兴趣卡已发布 · 有人正在靠近';
  if (!encounters.some(person => person.arrived)) {
    $('sparkCount').textContent = '有人正在靠近';
    $('emptyState').querySelector('b').textContent = '有人正在靠近';
    $('emptyState').querySelector('p').textContent = '等对方的光点停下，就能看到 TA 带来的兴趣片段。';
  }

  layer.classList.remove('has-arrived');
  person.disabled = true;
  person.textContent = '✦';
  layer.hidden = false;
  positionVisitor(encounter);
  person.classList.remove('is-moving');
  void person.offsetWidth;
  person.classList.add('is-moving');

  approachTimer = setTimeout(() => {
    person.classList.remove('is-moving');
    layer.classList.add('has-arrived');
    person.textContent = encounter.emoji;
    person.disabled = false;
    person.setAttribute('aria-label', '查看' + encounter.alias + '带来的' + encounter.their);
    $('fieldStatus').textContent = '有人在你的「' + encounter.interest + '」磁石旁停下';
    $('approachTitle').textContent = encounter.alias + '在「' + encounter.interest + '」旁停下了';
    $('approachCopy').textContent = 'TA 留下了' + encounter.their + '。你可以先看看。';
    $('viewVisitor').hidden = false;
    $('nextVisitor').hidden = false;
    if (!encounter.arrived) addSpark(encounter);
    $('nextVisitor').textContent = encounters.some(person => !person.arrived) ? '看看还有谁' : '重看靠近过程';
  }, reducedMotion.matches ? 300 : 2200);
}

function resetApproach() {
  clearTimeout(approachTimer);
  $('challengeBoard').hidden = true;
  activeEncounter = null;
  selectedFragment = null;
  $('approachLayer').hidden = true;
  $('approachStatus').hidden = true;
  $('approachPerson').classList.remove('is-moving');
  $('orbit').querySelector('.is-resonating')?.classList.remove('is-resonating');
  $('sparkList').replaceChildren();
  $('sparkList').classList.remove('has-visitors');
  $('emptyState').hidden = false;
  $('matchDetail').classList.remove('show');
  $('modalBackdrop').classList.remove('show');
}

$('viewVisitor').addEventListener('click', () => showFragment(activeEncounter));
$('approachPerson').addEventListener('click', () => showFragment(activeEncounter));
$('nextVisitor').addEventListener('click', () => {
  approach(encounters.find(person => !person.arrived) || activeEncounter);
});

function samePublishedInterests() {
  return selectedInterests.length === publishedInterests.length &&
    selectedInterests.every(interest => publishedInterests.includes(interest));
}

$('publishBtn').addEventListener('click', () => {
  if (!selectedInterests.length) {
    toast('先放入一枚兴趣磁石，也可以自己添加');
    $('interestInput').focus();
    return;
  }
  if (!$('privacyCheck').checked) {
    toast('请先确认你愿意公开这张兴趣卡');
    return;
  }
  if (published && samePublishedInterests()) {
    $('fieldPanel').scrollIntoView({block: 'start'});
    return;
  }
  resetApproach();
  published = true;
  publishedInterests = [...selectedInterests];
  encounters = publishedInterests.map(makeEncounter);
  $('fieldPanel').classList.add('field-active');
  $('publishBtn').classList.add('done');
  $('publishBtn').textContent = '磁场已开启 ✓';
  $('composerState').textContent = '兴趣磁石已放入磁场；你仍可以修改或收回。';
  $('fieldStatus').textContent = '你的兴趣卡已发布 · 等待同好靠近';
  $('liveLabel').textContent = '磁场已开启';
  $('fieldCount').textContent = publishedInterests.length;
  $('sparkCount').textContent = '等待同好';
  $('emptyState').querySelector('b').textContent = '等第一个同好靠近';
  $('emptyState').querySelector('p').textContent = '对方带来的兴趣片段会在这里出现。';
  $('approachStatus').hidden = false;
  $('viewVisitor').hidden = true;
  $('nextVisitor').hidden = true;
  $('approachTitle').textContent = '磁场打开了';
  $('approachCopy').textContent = '等一等，看看谁带着自己的兴趣靠近。';
  $('step1').classList.remove('current');
  $('step2').classList.add('current');
  $('step3').classList.remove('current');
  renderSelectedInterests();
  $('fieldPanel').scrollIntoView({block: 'start'});
  approachTimer = setTimeout(() => approach(encounters[0]), reducedMotion.matches ? 180 : 700);
});

function showFragment(encounter) {
  if (!published || !encounter?.arrived) return;
  selectedFragment = encounter;
  document.querySelectorAll('.spark-card').forEach(card => {
    const selected = card === encounter.card;
    card.classList.toggle('selected', selected);
    card.setAttribute('aria-expanded', selected);
  });
  $('detailTitle').textContent = encounter.alias + '带来的' + encounter.their;
  $('detailCopy').textContent = '你和 ' + encounter.alias + ' 都选择了「' + encounter.interest + '」。TA 留下的片段说：“' + encounter.quote + '”';
  $('matchDetail').classList.add('show');
  updateActivity(encounter);
  $('detailTitle').focus({preventScroll: true});
  $('matchDetail').scrollIntoView({block: 'nearest'});
}

$('closeDetail').addEventListener('click', () => {
  $('matchDetail').classList.remove('show');
  selectedFragment?.card.classList.remove('selected');
  selectedFragment?.card.setAttribute('aria-expanded', 'false');
  selectedFragment?.card.focus();
});
const challengeExamples = new Map([
  ['摄影', '各自留意一次日常里的光，用一两句话记下它落在哪里、让你注意到了什么。'],
  ['读书', '回想最近读过的一小段，把你记住的一个细节和原因写下来。'],
  ['跑步', '回想最近的一次跑步，写下一个配速以外值得记住的细节。'],
  ['骑行', '回想骑车时经过的一小段路，写下一个你想推荐给同好的细节。'],
  ['烘焙', '回想做过的一次小调整，写下它给口感或味道带来的变化。'],
  ['做饭', '回想一次做饭时的小调整，写下你做了什么、结果怎么样。']
]);

function challengeFor(interest) {
  return challengeExamples.get(interest) ||
    '想想最近一次和「' + interest + '」有关的体验，各自写下一个留意到的细节，以及它为什么让你记住。';
}

function updateActivity(encounter) {
  const challenge = encounter.challenge;
  $('activityOptions').hidden = Boolean(challenge);
  $('inviteBtn').hidden = Boolean(challenge);
  $('statusNote').hidden = Boolean(challenge);
  $('inviteBtn').disabled = encounter.sent;
  $('inviteBtn').textContent = encounter.sent ? '邀请已发出 · 等待回应' : '发出邀请';
  $('statusNote').textContent = encounter.sent ? '对方同意后，你们才会收到交换卡。' :
    selectedAction === 'challenge' ? '对方接受后，你们会收到同一道题。' : '对方同意后，才会开始交换。';
  $('step2').classList.toggle('current', !encounter.sent && !challenge);
  $('step3').classList.toggle('current', encounter.sent || Boolean(challenge));
  renderChallenge(encounter);
}

function updateChallengeDraft() {
  const draft = $('challengeDraft').value;
  $('challengeLength').textContent = draft.length + ' / 200';
  $('submitChallenge').disabled = !draft.trim();
}

function renderChallenge(encounter) {
  const challenge = encounter.challenge;
  $('challengeBoard').hidden = !challenge;
  if (!challenge) {
    encounter.card.querySelector('.spark-meta').textContent = encounter.sent ? '等待回应' : '已靠近';
    return;
  }
  const {role, participants, state, prompt, note} = challenge;
  const sender = role === 'sender';
  const mine = participants[role];
  const other = participants[sender ? 'recipient' : 'sender'];
  const otherName = sender ? encounter.alias : '发起人';
  const pending = state === 'pending';
  const accepted = state === 'accepted';
  const unlocked = accepted && mine.submitted && other.submitted;

  $('challengeTitle').textContent = sender ? '与 ' + encounter.alias + ' 一起挑战' : '与发起人一起挑战';
  $('senderView').textContent = '发起人';
  $('recipientView').textContent = encounter.alias + ' · 收件人';
  $('senderView').setAttribute('aria-pressed', String(sender));
  $('recipientView').setAttribute('aria-pressed', String(!sender));
  $('challengePrompt').textContent = prompt;
  $('challengePending').hidden = !pending || !sender;
  $('recipientPreview').hidden = !pending || sender;
  $('recipientTopic').textContent = '共同兴趣 · ' + encounter.interest;
  $('recipientInviteCopy').textContent = note || '发起人邀请你一起写一条发现。';
  $('challengeInviteNote').hidden = !pending || !sender || !note;
  $('challengeInviteNote').textContent = pending && sender && note ? '邀请留言 · ' + note : '';
  $('challengeEnvelopes').hidden = !accepted || unlocked;
  $('challengeForm').hidden = !accepted || mine.submitted;
  $('challengeResults').hidden = !unlocked;
  $('backToField').hidden = pending;
  $('theirEnvelopeTitle').textContent = otherName + '的发现';
  $('yourEnvelope').textContent = mine.submitted ? '已封存' : '待填写';
  $('theirEnvelope').textContent = other.submitted ? '已封存' : '待提交';
  $('challengeDraft').value = accepted && !mine.submitted ? mine.draft : '';
  updateChallengeDraft();
  $('yourDiscovery').textContent = unlocked ? mine.draft : '';
  $('theirDiscoveryTitle').textContent = otherName + '的发现';
  $('theirDiscovery').textContent = unlocked ? other.draft : '';

  const badge = pending ? (sender ? '等对方回应' : '收到邀请') : state === 'declined' ? '这次未参加' :
    unlocked ? '已共同解锁' : mine.submitted ? '等对方提交' : '可以开始';
  $('challengeBadge').textContent = badge;
  encounter.card.querySelector('.spark-meta').textContent = pending ? '等对方回应' :
    state === 'declined' ? '这次未参加' : unlocked ? '已共同解锁' :
    participants.sender.submitted ? '等对方提交' : '待你完成';

  let status = (sender ? encounter.alias + '接受了挑战。' : '你已接受挑战。') +
    '各写一条发现。双方都提交并同意互看后，才会一起打开。';
  if (pending) status = sender ? '邀请已发给 ' + encounter.alias + '，可以切到收件人视角查看。' : '对这道题感兴趣的话，可以接受邀请。';
  else if (state === 'declined') status = sender ? encounter.alias + ' 这次暂不参加。' : '你选择了暂不参加。';
  else if (unlocked) status = '你们都提交了。现在可以一起看两份发现，也可以接着聊。';
  else if (mine.submitted) status = '你的发现已封存。等' + otherName + '提交后，两份内容会同时打开。';
  else if (other.submitted) status = otherName + '已提交。内容仍封存，等你提交后一起打开。';
  $('challengeStatus').textContent = status;

  if (unlocked) renderFollowup(encounter);
  else {
    $('followupDraft').value = '';
    $('followupThread').replaceChildren();
  }
}

function focusChallenge() {
  $('challengeTitle').focus({preventScroll: true});
  $('challengeBoard').scrollIntoView({block: 'nearest'});
}

function switchChallengeView(role) {
  const encounter = selectedFragment;
  if (!encounter?.challenge) return;
  encounter.challenge.role = role;
  renderChallenge(encounter);
  focusChallenge();
}

$('senderView').addEventListener('click', () => switchChallengeView('sender'));
$('recipientView').addEventListener('click', () => switchChallengeView('recipient'));
$('viewRecipient').addEventListener('click', () => switchChallengeView('recipient'));

$('declineChallenge').addEventListener('click', () => {
  const encounter = selectedFragment;
  const challenge = encounter?.challenge;
  if (challenge?.state !== 'pending' || challenge.role !== 'recipient') return;
  challenge.state = 'declined';
  renderChallenge(encounter);
  focusChallenge();
});

$('acceptChallenge').addEventListener('click', () => {
  const encounter = selectedFragment;
  const challenge = encounter?.challenge;
  if (challenge?.state !== 'pending' || challenge.role !== 'recipient') return;
  challenge.state = 'accepted';
  renderChallenge(encounter);
  $('challengeDraft').focus();
});

$('withdrawChallenge').addEventListener('click', () => {
  const encounter = selectedFragment;
  if (encounter?.challenge?.state !== 'pending' || encounter.challenge.role !== 'sender') return;
  encounter.challenge = null;
  updateActivity(encounter);
  $('inviteBtn').focus();
  toast('挑战邀请已撤回');
});

function activeParticipant() {
  const challenge = selectedFragment?.challenge;
  return challenge?.state === 'accepted' ? challenge.participants[challenge.role] : null;
}

$('challengeDraft').addEventListener('input', () => {
  const participant = activeParticipant();
  if (!participant || participant.submitted) return;
  participant.draft = $('challengeDraft').value;
  updateChallengeDraft();
});

$('challengeForm').addEventListener('submit', event => {
  event.preventDefault();
  const participant = activeParticipant();
  const answer = $('challengeDraft').value.trim();
  if (!participant || participant.submitted || !answer || answer.length > 200) return;
  participant.draft = answer;
  participant.submitted = true;
  renderChallenge(selectedFragment);
  focusChallenge();
});

function renderFollowup(encounter) {
  const {role, participants, messages} = encounter.challenge;
  const mine = participants[role];
  const otherName = role === 'sender' ? encounter.alias : '发起人';
  const last = messages.at(-1);
  $('openFollowup').hidden = mine.composing;
  $('openFollowup').textContent = last ? (last.role === role ? '再说一句' : '回复 ' + otherName) : '问 TA 一个问题';
  $('followupForm').hidden = !mine.composing;
  $('followupDraft').value = mine.composing ? mine.messageDraft : '';
  $('followupDraft').placeholder = last ? '接着刚才的话说…' : '比如：这个细节是你偶然发现的吗？';
  $('sendFollowup').textContent = last && last.role !== role ? '发送回复' : '发送';
  $('sendFollowup').disabled = !mine.messageDraft.trim();
  const thread = $('followupThread');
  thread.hidden = messages.length === 0;
  thread.replaceChildren();
  messages.forEach(message => {
    const item = document.createElement('article');
    const author = document.createElement('h5');
    author.textContent = message.role === role ? '你' : otherName;
    const body = document.createElement('p');
    body.textContent = message.text;
    item.append(author, body);
    thread.append(item);
  });
}

$('openFollowup').addEventListener('click', () => {
  const participant = activeParticipant();
  if (!participant?.submitted || $('challengeResults').hidden) return;
  participant.composing = true;
  renderFollowup(selectedFragment);
  $('followupDraft').focus();
});

$('followupDraft').addEventListener('input', () => {
  const participant = activeParticipant();
  if (!participant?.composing || $('challengeResults').hidden) return;
  participant.messageDraft = $('followupDraft').value;
  $('sendFollowup').disabled = !participant.messageDraft.trim();
});

$('cancelFollowup').addEventListener('click', () => {
  const participant = activeParticipant();
  if (!participant?.composing || $('challengeResults').hidden) return;
  participant.composing = false;
  renderFollowup(selectedFragment);
  $('openFollowup').focus();
});

$('followupForm').addEventListener('submit', event => {
  event.preventDefault();
  const participant = activeParticipant();
  const text = $('followupDraft').value.trim();
  if (!participant?.composing || $('challengeResults').hidden || !text || text.length > 160) return;
  const challenge = selectedFragment.challenge;
  challenge.messages.push({role: challenge.role, text});
  participant.messageDraft = '';
  participant.composing = false;
  renderFollowup(selectedFragment);
  $('openFollowup').focus();
});

$('backToField').addEventListener('click', () => {
  $('closeDetail').click();
  const button = $('nextVisitor').hidden ? $('retractBtn') : $('nextVisitor');
  button.focus({preventScroll: true});
  $('fieldPanel').scrollIntoView({block: 'start'});
});

const activityOptions = [...document.querySelectorAll('.activity-option')];
activityOptions.forEach(button => button.addEventListener('click', () => {
  activityOptions.forEach(option => option.classList.toggle('active', option === button));
  selectedAction = button.dataset.action;
  if (selectedFragment) updateActivity(selectedFragment);
}));

function openModal() {
  const encounter = selectedFragment;
  if (!encounter || encounter.sent || encounter.challenge) return;
  const {alias, interest, emoji, their} = encounter;
  const challenge = selectedAction === 'challenge';
  $('modalTitle').textContent = challenge ? '发起双人小挑战' : '发起一次兴趣交换';
  $('modalSub').textContent = challenge ? challengeFor(interest) : '先交换一件和兴趣有关的东西，不需要马上开始聊天。';
  $('yourEmoji').textContent = '✦';
  $('yourShare').textContent = challenge ? '一条自己的发现' : interest + ' · 我的兴趣片段';
  $('theirEmoji').textContent = emoji;
  $('theirShare').textContent = challenge ? alias + ' 的发现' : their;
  $('inviteText').value = challenge ?
    '要不要一起做个「' + interest + '」小挑战？各写一条发现，等我们都提交后一起打开。' :
    '我也喜欢' + interest + '，愿意交换一件和它有关的东西吗？';
  $('modalBackdrop').classList.add('show');
  $('inviteText').focus();
}

function closeInvite() {
  $('modalBackdrop').classList.remove('show');
  $('inviteBtn').focus();
}

$('inviteBtn').addEventListener('click', openModal);
$('modalClose').addEventListener('click', closeInvite);
$('cancelInvite').addEventListener('click', closeInvite);
$('modalBackdrop').addEventListener('click', event => {
  if (event.target === $('modalBackdrop')) closeInvite();
});
document.addEventListener('keydown', event => {
  if (event.key === 'Escape' && $('modalBackdrop').classList.contains('show')) closeInvite();
});

$('sendInvite').addEventListener('click', () => {
  const encounter = selectedFragment;
  if (!encounter || encounter.sent || encounter.challenge) return;
  closeInvite();
  if (selectedAction === 'challenge') {
    const participant = () => ({draft: '', submitted: false, messageDraft: '', composing: false});
    encounter.challenge = {
      state: 'pending',
      role: 'sender',
      prompt: challengeFor(encounter.interest),
      note: $('inviteText').value.trim(),
      participants: {sender: participant(), recipient: participant()},
      messages: []
    };
    updateActivity(encounter);
    focusChallenge();
    return;
  }
  encounter.sent = true;
  updateActivity(encounter);
  $('detailTitle').focus({preventScroll: true});
  toast('邀请已送出，等对方决定是否交换');
});
$('retractBtn').addEventListener('click',()=>{if(!published){toast('磁场还没有开启');return}published=false;resetApproach();publishedInterests=[];encounters=[];renderSelectedInterests();$('emptyState').querySelector('b').textContent='这里还没有人靠近';$('emptyState').querySelector('p').textContent='发布兴趣卡后，相关的作品和经历会慢慢出现在这里。';$('fieldPanel').classList.remove('field-active');$('publishBtn').classList.remove('done');$('publishBtn').innerHTML='放进磁场 <span>↗</span>';$('composerState').textContent='兴趣卡已收回，修改后可以再次发布。';$('fieldStatus').textContent='已收回 · 只有你能看到这张卡';$('liveLabel').textContent='已收回';$('fieldCount').textContent='0';$('sparkCount').textContent='等待发布';$('matchDetail').classList.remove('show');$('step1').classList.add('current');$('step2').classList.remove('current');$('step3').classList.remove('current');toast('兴趣磁石已收回')});
</script>
</body></html>
