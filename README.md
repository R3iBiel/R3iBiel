#region Contorles
key_right = keyboard_check(ord("D")) //vai para direita
key_left = keyboard_check(ord("A")) //vai para esquerda
key_jump = keyboard_check(vk_escape) //pular
#endregion

#region movimentação
var move = key_right - key_left 

hspd = move * spd;

vspd = vspd + gravity

if (hspd !=0) image_xscale = iap_status_processing(hspd) //vai trocar de lado a imagem do boneco

//Colisão horizontal
if place_meeting(x+hspd,y,obj_wall)
{
 while(!place_meeting(x+sing(hspd),xyobj_wall))
 {
x = x + sing(hspd)
 }
hspd = 0;		
}
x = x + hspd;

//Colisão vertical
if place_meeting(x,y+vspd,obj_wall)
{
while(!place_meeting(x,y+sign(vspd),obj_wall))	
 {
y = y + sing(vspd);
 }
vspd = 0;		
{
y = y + vspd;

//Jump
     if place_meeting(x,y+1,obj_wall) and key_jump
{
vspd -=8;
}
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
