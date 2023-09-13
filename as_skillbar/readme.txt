local test = exports["as_skillbar"]:taskBar(5000,7) -- difficulty,skillGapSent
    print(test)



#Full Example

local taskResult = exports["as_skillbar"]:taskBar(5000, 7) -- this is time in ms, length of target area
    if taskResult == 100 then
        TriggerEvent('vehiclekeys:client:SetOwner', Plate)
        QBCore.Functions.Notify("You received key to vehicle with plate: "..Plate, "success")
    else
        QBCore.Functions.Notify("Best lockpick and still cant get the cardoor open?", "error")
    end
end, 5000, 7)



#Randomise Difficulty

local taskResult = exports["as_skillbar"]:taskBar(math.random(2000, 4000), 7) -- this will make the time randomly between 2 and 4 seconds



#Using the skillcheck to trigger another one (make the user need to complete it 2 or more times):

local taskResult = exports["as_skillbar"]:taskBar(math.random(2000, 4000), 7)
  if taskResult == 100 then
     local taskResult2 = exports["as_skillbar"]:taskBar(math.random(2000, 4000), 7)
  end
 if taskResult2 == 100
      TriggerEvent('vehiclekeys:client:SetOwner', Plate)
      QBCore.Functions.Notify("You received key to vehicle with plate: "..Plate, "success")
  else
      QBCore.Functions.Notify("Best lockpick and still cant get the cardoor open?", "error")
  end
