# 
QB CORE STRESS OFF
DELETE STRESS FOR QB-CORE FIVEM SYSTEM


HOW TO DELETE ? 

Its eazy ......

Go **[qb]/qb-hud** and find **client.lua**

STEP 2 

Find 907 line this line begins **-- Stress Gain**

STEP 3 

you can turn it off or delete it but I recommend turning it off like this

```
-- Stress Gain

--CreateThread(function() -- Speeding
   -- while true do
       -- if LocalPlayer.state.isLoggedIn then
           -- local ped = PlayerPedId()
            --if IsPedInAnyVehicle(ped, false) then
               -- local veh = GetVehiclePedIsIn(ped, false)
               -- local vehClass = GetVehicleClass(veh)
               -- local speed = GetEntitySpeed(veh) * speedMultiplier

               -- if vehClass ~= 13 and vehClass ~= 14 and vehClass ~= 15 and vehClass ~= 16 and vehClass ~= 21 then
                    --local stressSpeed
                    --if vehClass == 8 then
                       -- stressSpeed = config.MinimumSpeed
                   -- else
                       -- stressSpeed = seatbeltOn and config.MinimumSpeed or config.MinimumSpeedUnbuckled
                   -- end
                   -- if speed >= stressSpeed then
                       -- TriggerServerEvent('hud:server:GainStress5', math.random(1, 3))
                   -- end
               -- end
          --  end
        --end
       -- Wait(10000)
   -- end
---end)

-- local function IsWhitelistedWeaponStress(weapon)
   -- if weapon then
       -- for _, v in pairs(config.WhitelistedWeaponStress) do
            --if weapon == v then
              --  return true
           -- end
       -- end
   -- end
   -- return false
--end

--CreateThread(function() -- Shooting
   -- while true do
      --  if LocalPlayer.state.isLoggedIn then
         --   local ped = PlayerPedId()
          --  local weapon = GetSelectedPedWeapon(ped)
          --  if weapon ~= `WEAPON_UNARMED` then
               -- if IsPedShooting(ped) and not IsWhitelistedWeaponStress(weapon) then
                  --  if math.random() < config.StressChance then
                      --  TriggerServerEvent('hud:server:GainStress', math.random(1, 3))
                  --  end
               -- end
          --  else
              --  Wait(1000)
           -- end
       -- end
       -- Wait(8)
  ---  end
-- end)

-- Stress Screen Effects

-- local function GetBlurIntensity(stresslevel)
   -- for _, v in pairs(config.Intensity['blur']) do
       -- if stresslevel >= v.min and stresslevel <= v.max then
          --  return v.intensity
       -- end
   -- end
   -- return 1500
--end

--local function GetEffectInterval(stresslevel)
   -- for _, v in pairs(config.EffectInterval) do
       -- if stresslevel >= v.min and stresslevel <= v.max then
           -- return v.timeout
      -- end
   -- end
   -- return 60000
--end

--CreateThread(function()
   -- while true do
      --  local ped = PlayerPedId()
      --  local effectInterval = GetEffectInterval(stress)
      --  if stress >= 100 then
         --   local BlurIntensity = GetBlurIntensity(stress)
        --    local FallRepeat = math.random(2, 4)
        --    local RagdollTimeout = FallRepeat * 1750
        --    TriggerScreenblurFadeIn(1000.0)
        --    Wait(BlurIntensity)
        --    TriggerScreenblurFadeOut(1000.0)

         --   if not IsPedRagdoll(ped) and IsPedOnFoot(ped) and not IsPedSwimming(ped) then
         --       SetPedToRagdollWithFall(ped, RagdollTimeout, RagdollTimeout, 1, GetEntityForwardVector(ped), 1.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0)
         --   end

         --   Wait(1000)
          --  for _ = 1, FallRepeat, 1 do
           --     Wait(750)
           --     DoScreenFadeOut(200)
           --     Wait(1000)
             --   DoScreenFadeIn(200)
            --    TriggerScreenblurFadeIn(1000.0)
            --    Wait(BlurIntensity)
            --    TriggerScreenblurFadeOut(1000.0)
        --    end
       -- elseif stress >= config.MinimumStress then
         --   local BlurIntensity = GetBlurIntensity(stress)
         --   TriggerScreenblurFadeIn(1000.0)
         --   Wait(BlurIntensity)
         --   TriggerScreenblurFadeOut(1000.0)
      --  end
      --  Wait(effectInterval)
   -- end
--end)
```

STEP 4

DONE
