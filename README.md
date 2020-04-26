# tactLayers
Abstract javascript game

JavaScript and HTML game designed to experiment with tactical level command and control
of multiple semi-autonomous assets.
- Designed as a "rock, paper, scissor" style game. Each asset has a vice and a victim.
- Each asset has a damage spot it can attack within
  - Assets attack automatically in a predictable pattern
  - Assets move in a predictable pattern
  - Assets move within their "layer"

ASSETS:
Infinite Stamina: (Can move continuously)
  UGV Heavy -- slow but heavily armored and high damage
  UGV Light -- fast but lower armor and mid damage

  UAV Eye -- Spots for friendly assets:
    -- UGV Heavy attack in all directions while overhead
    -- UGV Light

    -- UAV Drop can hit UGVall
    -- Infantry can attack UGV

  UAV Drop -- Can attack Infantry and turrets
    -- Drops with random probability in cardinal directions and under
    -- 1 in 5 chance

Limited Stamina: (Move - Stop - Move)
  Infantry -- Control UxS (Must be alive to use UxS)
    -- Can attack UGVL
    -- Can attack UAV E
    -- Can attack Infantry

Immobile: (Cannot move)
  UGT -- Can attack at range 180 degrees.
    -- Can attack within the Infantry and UGV layer


BATTLESPACES:

UG - Ground Vehicles and Turrets
Infantry - Operators and Infantry
UA - UAV

Interfaces:
  Air to Ground:
  -- UAV D can attack Infantry and Turrets

  Ground to Groud:
  -- UGV all can attack Infantry
  -- Infantry can attack UGV L
  -- Turrets can attack Infantry and UGVall

  Ground to Air:
  -- Infantry can attack UAV D
  --UGV H can attack UAVall
  
