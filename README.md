UI.AddSubTab(["Visuals", "SUBTAB_MGR"], "Kiana's AimbotLog")
var path = ["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog"];
UI.AddCheckbox(path, "Fire log" );
UI.AddCheckbox(path, "Damage log" );
UI.AddCheckbox(path, "Miss log" );
UI.AddCheckbox(path, "Saying log" );

hitboxes = [
    'body',
    'head',
    'chest',
    'stomach',
    'left arm',
    'right arm',
    'left leg',
    'right leg',
    'neck'
];
var scriptitems = ( ["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog"]);
var shots = 0;
var misses = 0;
var predicthc = 0;
var safety1 = 0;
var hitboxName = "";
var hitbox = "";
var choked1 = 0;
var exploit = 0;
var logs = [];
var logsct = [];
var logsalpha = [];
var nlogs = [];
function getHitboxName(index)
{
    switch (index)
    {
        case 0:
            hitboxName = "head";
            break;
        case 1:
            hitboxName = "head";
            break;
        case 2:
            hitboxName = "stomach";
            break;
        case 3:
            hitboxName = "stomach";
            break;
        case 4:
            hitboxName = "stomach";
            break;
        case 5:
            hitboxName = "chest";
            break;
        case 6:
            hitboxName = "chest";
            break;
        case 7:
            hitboxName = "left leg";
            break;
        case 8:
            hitboxName = "right leg";
            break;
        case 9:
            hitboxName = "left leg";
            break;
        case 10:
            hitboxName = "right leg";
            break;
        case 11:
            hitboxName = "left leg";
            break;
        case 12:
            hitboxName = "right leg";
            break;
        case 13:
            hitboxName = "left arm";
            break;
        case 14:
            hitboxName = "right arm";
            break;
        case 15:
            hitboxName = "left arm";
            break;
        case 16:
            hitboxName = "left arm";
            break;
        case 17:
            hitboxName = "right arm";
            break;
        case 18:
            hitboxName = "right arm";
            break;
        default:
            hitboxName = "body";
    }
    return hitboxName;
}
function HitgroupName(index) {
    return hitboxes[index] || 'body';
}

var target = -1;
var shots_fired = 0;
var hits = 0;
var misses = 0;
var lastUpdate = 0;
var logged = false;
var myPing = Math.floor(Local.Latency()*1000/1.5);
var tickrate = Globals.Tickrate()
var jopadeath = Math.floor(Local.Latency()*1000/2.5);



function ragebot_fire() {
    predicthc = Event.GetInt("hitchance");
    safety1 = Event.GetInt("safepoint");
    hitboxName = getHitboxName(Event.GetInt("hitbox"));
    exploit = (Event.GetInt("exploit")+1).toString();
  target = Event.GetInt("target_index");
  shots_fired++;
  logged = false;
  lastUpdate = Globals.Curtime();
    target_damage = Event.GetInt("dmg_health");

        if (UI.GetValue(["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog", "Fire log"])) {
      if (target) {
       Cheat.PrintLog("[Bronyaware] 休伯利安号主炮充能完毕 开始射击 " + Entity.GetName(target) + ", 目标: " + hitboxName + "  伤害: " +Ragebot.GetTarget() + "  命中概率: " + Ragebot.GetTargetHitchance( ) + "  bt: 0 (0 tks)  hp: false" + "\n",[147, 112, 219,255])
}
}
}
function hitlog() {
    var hit = Entity.GetEntityFromUserID(Event.GetInt("userid"));
    var attacker = Entity.GetEntityFromUserID(Event.GetInt("attacker"));
    if (attacker == Entity.GetLocalPlayer() && hit == target) hits++;

    var hittype = "Hit ";
    me = Entity.GetLocalPlayer();
    hitbox = Event.GetInt('hitgroup');
    target_damage = Event.GetInt("dmg_health");
    target_health = Event.GetInt("health");
    victim = Event.GetInt('userid');
    attacker = Event.GetInt('attacker');
    weapon = Event.GetString('weapon');
    victimIndex = Entity.GetEntityFromUserID(victim);
    attackerIndex = Entity.GetEntityFromUserID(attacker);
    name = Entity.GetName(victimIndex);
      var simtime = Globals.Tickcount() % 17;

    var flags = "";

    if (exploit == 2)
      flags += "T";

    flags += "B";

    if (hitbox == 1)
      flags += "H";

      if (safety1 == 1) {
          safety1 = "1";
      }
      else {
          safety1 = "0";
      }


dead = Event.GetInt("health") <= 0
      if (Event.GetInt("health") <= 0) {
        var simtime = Globals.Tickcount() % 16;
        logged = true;
        var issafe = "1";
        var dead = " (死亡)";
      }

      else if (Event.GetInt("health") >= 1) {
        var dead = "";
      }

n4m3 = Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid")))
      if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "   " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "      " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "         " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "            " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "               " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                  " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                     " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                        " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                           " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                              " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                                 " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                                    " ) 
        n4m3 = "?";
      else if (Entity.GetName(Entity.GetEntityFromUserID(Event.GetInt("userid"))) == "                                       " ) 
        n4m3 = "?";




    if (weapon == "hegrenade")
      hittype = "";
    else if (weapon == "inferno")
      hittype = "";
    else if (weapon == "knife")
      hittype = "";
    else if (weapon == "sawedoff")
      hittype = "";
    else if (weapon == "xm1014")
      hittype = "";
    else if (weapon == "nova")
      hittype = "";
    else if (weapon == "mag7")
      hittype = "";

    if (me == attackerIndex && me != victimIndex) {1

    if (hittype == "Hit ") {
        if (UI.GetValue(["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog", "Damage log"])) {
        Cheat.PrintLog("[Bronyaware] 休伯利安号主炮命中目标! " +  n4m3 + ", 部位: " + HitgroupName(Event.GetInt("hitgroup")) + "  伤害: " + Event.GetInt("dmg_health") + "  剩余血量: " + Event.GetInt("health") + dead + "\n",[100, 149, 237,255])
        Cheat.PrintLog("Hit " +  n4m3 + " in the " + HitgroupName(Event.GetInt("hitgroup")) + " for " + Event.GetInt("dmg_health") + " damage (" + Event.GetInt("health") + " health remaining)" + "\n",[255, 255, 255,255])
        }
    }
    else {
        Cheat.PrintLog("[Bronyaware] 休伯利安号主炮命中目标! " +  n4m3 + ", 部位: " + HitgroupName(Event.GetInt("hitgroup")) + "  伤害: " + Event.GetInt("dmg_health") + "  剩余血量: " + Event.GetInt("health") + dead + "\n",[100, 149, 237,255])
        Cheat.PrintLog("Hit " +  n4m3 + " in the " + HitgroupName(Event.GetInt("hitgroup")) + " for " + Event.GetInt("dmg_health") + " damage (" + Event.GetInt("health") + " health remaining)" + "\n",[255, 255, 255,255])
    }

        logsct.push(Globals.Curtime());
        logsalpha.push(255);
    }

  if (shots == 99)
    shots = 0;
  else
    shots++;



}

function removelogs() {
    if (logs.length > 6) {
        logs.shift();
        logsct.shift();
        logsalpha.shift();
    }

    if (logsct[0] + 6.5 < Globals.Curtime()) {
        logsalpha[0] -= Globals.Frametime() * 600;
        if (logsalpha[0] < 0) {
            logs.shift();
            logsct.shift();
            logsalpha.shift();
        }
    }
}

function item_purchase() {

    logsct.push(Globals.Curtime());
    logsalpha.push(255);
}

function onDraw() {
    if (!World.GetServerString()) return;
    var font = Render.GetFont("verdana.ttf", 10, true);


    for (i = 0; i < logs.length; i++) {
        Render.String(4, 4 + 13*i, 0, logs[i], [0, 0, 0, logsalpha[i]], font);
        Render.String(3, 3 + 13*i, 0, logs[i], [255, 255, 255, logsalpha[i]], font);
    }

    if (shots_fired > hits && (Globals.Curtime() - lastUpdate > 0.09)) {
      if (Globals.Curtime() - lastUpdate > 0) {
        shots_fired = 0;
        hits = 0;
        }


      if (!logged) {
        var simtime = Globals.Tickcount() % 16;
        logged = true;
        var issafe = "1";
        var reason = "解析器";
        if (safety1 == 0) {
          issafe = "0";
        }

        if (safety1 == true && predicthc <= 74)
            reason = "航速过快导致射击误差";
        else if (safety1 == true && predicthc >= 75)
            reason = "解析器";


        var flags = "";
       

        if (exploit == 2)
          flags += "T";

          flags += "B";
    target_damage = Event.GetInt("dmg_health");
        if (Event.GetInt("dmg_health") == undefined)
target_damage = "0"

n4me = Entity.GetName(target)
      if (Entity.GetName(target) == "   " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "      " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "         " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "            " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "               " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                  " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                     " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                        " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                           " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                              " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                                 " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                                    " ) 
        n4me = "?";
      else if (Entity.GetName(target) == "                                       " ) 
        n4me = "?";


misslog = misses
      if (misses == "0" ) 
       misslog = "努力是不会背叛自己的, 虽然梦想有时会背叛自己。";
      else if (misses == "1" ) 
        misslog = "我不努力, 就见不到你了啊。";
      else if (misses == "2" ) 
        misslog = "我不相信人类......但是, 我相值人类的“可能性”";
      else if (misses == "3" ) 
        misslog = "只要学不死, 就往死里学。";
      else if (misses == "4" ) 
        misslog = "即使看不到未来，即使看不到希望，也依然相信自己。";
      else if (misses == "5" ) 
        misslog = "After all, tomorrow is another day!";



            if (UI.GetValue(["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog", "Miss log"])) {
        Cheat.PrintLog("[Bronyaware] 休伯利安号主炮未命中目标... " + n4me + "，目标 " + hitboxName + "  原因 " + reason  + "\n",[255, 253, 166,255])
        }

    if (UI.GetValue(["Visuals", "Kiana's AimbotLog", "Kiana's AimbotLog", "Saying log"])) {
        Cheat.PrintLog(misslog + "\n",[255, 255, 255,255])
        }

        logsct.push(Globals.Curtime());
            logsalpha.push(255);
        if (shots == 99)
          shots = 0;
        else
          shots++;

  if (misses >= 5)
    misses = 0;
  else
    misses++;
      }
    }
}







     


function main1() {
    Global.RegisterCallback("ragebot_fire", "ragebot_fire");
    Global.RegisterCallback("item_purchase", "item_purchase");
  Global.RegisterCallback("player_hurt", "hitlog");
    Global.RegisterCallback("Draw", "onDraw");
    Global.RegisterCallback("Draw", "removelogs");
}

main1();
