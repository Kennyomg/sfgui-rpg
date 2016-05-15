#SFML + SFGUI RPG

At the moment this project is for learning Design Patterns.

I'm trying out the Strategy Design.

##Library

- Guis
  - **Gui**.h
  - Gui.cpp
- Managers
  - **Manager**.h
  - Manager.cpp
- Scenes
  - **Scene**.h
  - Scene.cpp
- World Objects
  - Blocks
    - Behaviors
      - __*Destructable*__.h
      - Destructable.cpp
      - __*Lootable*__.h
      - Lootable.cpp
    - Environment
      - **BlockEnvironment**.h
        - : **Block**
      - BlockEnvironment.cpp
    - **Block**.h
    - Block.cpp
  - Entities
    - Behaviors
      - __*Killable*__.h
      - Killable.cpp
      - __*Lootable*__.h
      - Lootable.cpp
      - __*Tradeable*__.h
      - Tradeable.cpp
    - Monsters
    - Npcs
    - **Entity**.h
    - Entity.cpp
  - Items
    - Behaviors
      - Actions
        - Use
          - **Shoot**.h
            - : __*UseBehavior*__
          - Shoot.cpp
          - **Throw**.h
            - : __*UseBehavior*__
          - Throw.cpp
          - **Slash**.h
            - : __*UseBehavior*__
          - Slash.cpp
          - **Smash**.h
            - : __*UseBehavior*__
          - Smash.cpp
          - **Thrust**.h
            - : __*UseBehavior*__
          - Thrust.cpp
          - **Consume**.h
            - : __*UseBehavior*__
          - Consume.cpp
          - **NoUse**.cpp
            - : __*UseBehavior*__
          - NoUse.cpp
        - Equip
          - **Shoulders**.h
            - : __*EquipBehavior*__
          - Shoulders.cpp
          - **Feet**.h
            - : __*EquipBehavior*__
          - Feet.cpp
          - **Hands**.h
            - : __*EquipBehavior*__
          - Hands.cpp
          - **Chest**.h
            - : __*EquipBehavior*__
          - Chest.cpp
          - **Head**.h
            - : __*EquipBehavior*__
          - Head.cpp
          - **MainHand**.h
            - : __*EquipBehavior*__
          - MainHand.cpp
          - **OffHand**.h
            - : __*EquipBehavior*__
          - OffHand.cpp
          - **TwoHand**.h
            - : __*EquipBehavior*__
          - TwoHand.cpp
          - **AmmoSlot**.h
            - : __*EquipBehavior*__
          - AmmoSlot.cpp
          - **ItemSlot**.h
            - : __*EquipBehavior*__
          - ItemSlot.cpp
          - **NoEquip**.h
            - : __*EquipBehavior*__
          - NoEquip.cpp
        - Weight
          - **Heavy**.h
            - : __*WeightBehavior*__
          - Heavy.cpp
          - **Medium**.h
            - : __*WeightBehavior*__
          - Medium.cpp
          - **Light**.h
            - : __*WeightBehavior*__
          - Light.cpp
          - **NoWeight**.h
            - : __*WeightBehavior*__
          - NoWeight.cpp
      - __*EquipBehavior*__.h
      - EquipBehavior.cpp
      - __*UseBehavior*__.h
      - UseBehavior.cpp
      - __*WeightBehavior*__.h
      - WeightBehavior.cpp
      - __*Equipable*__.h
      - Equipable.cpp
      - __*Sellable*__.h
      - Sellable.cpp
      - __*Buyable*__.h
      - Buyable.cpp
    - Equipment
      - Weapons
        - Swords
          - **ItemSword**.h
            - : **ItemWeapon**
            - *useBehavior* = new **Slash**
            - *equipBehavior* = new **MainHand**
          - ItemSword.cpp
        - Axes
          - **ItemAxe**.h
            - : **ItemWeapon**
            - *useBehavior* = new **Slash**
            - *equipBehavior* = new **MainHand**
          - ItemAxe.cpp
        - Bows
          - **ItemBow**.h
            - : **ItemWeapon**
            - *useBehavior* = new **Shoot**
            - *equipBehavior* = new **TwoHand**
          - ItemBow.cpp
        - Knives
          - **ItemKnife**.h
            - : **ItemWeapon**
            - *useBehavior* = new **Thrust**
            - *equipBehavior* = new **MainHand**
          - ItemKnife.cpp
        - **ItemWeapon**.h
          - : **ItemEquipment**
        - ItemWeapon.cpp
      - Armors
        - Heavy
          - Bodies
            - **ItemArmorHeavyBody**.h
              - : **ItemArmorHeavy**
              - *equipBehavior* = new **Chest**
            - ItemArmorHeavyBody.cpp
          - Heads
            - **ItemArmorHeavyHead**.h
              - : **ItemArmorHeavy**
              - *equipBehavior* = new **Head**
            - ItemArmorHeavyHead.cpp
          - Shoulders
            - **ItemArmorHeavyShoulder**.h
              - : **ItemArmorHeavy**
              - *equipBehavior* = new **Shoulders**
            - ItemArmorHeavyShoulder.cpp
          - Gloves
            - **ItemArmorHeavyGlove**.h
              - : **ItemArmorHeavy**
              - *equipBehavior* = new **Hands**
            - ItemArmorHeavyGlove.cpp
          - Boots
            - **ItemArmorHeavyBoot**.h
              - : **ItemArmorHeavy**
              - *equipBehavior* = new **Feet**
            - ItemArmorHeavyBoot.cpp
          - **ItemArmorHeavy**.h
            - : **ItemEquipment**
            - *weightBehavior* = new **Heavy**
          - ItemArmorHeavy.cpp
        - Medium
          - Bodies
            - **ItemArmorMediumBody**.h
              - : **ItemArmorMedium**
              - *equipBehavior* = new **Chest**
            - ItemArmorMediumBody.cpp
          - Heads
            - **ItemArmorMediumHead**.h
              - : **ItemArmorMedium**
              - *equipBehavior* = new **Head**
            - ItemArmorMediumHead.cpp
          - Shoulders
            - **ItemArmorMediumShoulder**.h
              - : **ItemArmorMedium**
              - *equipBehavior* = new **Shoulders**
            - ItemArmorMediumShoulder.cpp
          - Gloves
            - **ItemArmorMediumGlove**.h
              - : **ItemArmorMedium**
              - *equipBehavior* = new **Hands**
            - ItemArmorMediumGlove.cpp
          - Boots
            - **ItemArmorMediumBoot**.h
              - : **ItemArmorMedium**
              - *equipBehavior* = new **Feet**
            - ItemArmorMediumBoot.cpp
          - **ItemArmorMedium**.h
            - : **ItemEquipment**
            - *weightBehavior* = new **Medium**
          - ItemArmorMedium.cpp
        - Light
          - Bodies
            - **ItemArmorLightBody**.h
              - : **ItemArmorLight**
              - *equipBehavior* = new **Chest**
            - ItemArmorLightBody.cpp
          - Heads
            - **ItemArmorLightHead**.h
              - : **ItemArmorLight**
              - *equipBehavior* = new **Head**
            - ItemArmorLightHead.cpp
          - Shoulders
            - **ItemArmorLightShoulder**.h
              - : **ItemArmorLight**
              - *equipBehavior* = new **Shoulders**
            - ItemArmorLightShoulder.cpp
          - Gloves
            - **ItemArmorLightGlove**.h
              - : **ItemArmorLight**
              - *equipBehavior* = new **Hands**
            - ItemArmorLightGlove.cpp
          - Boots
            - **ItemArmorLightBoot**.h
              - : **ItemArmorLight**
              - *equipBehavior* = new **Feet**
            - ItemArmorLightBoot.cpp
          - **ItemArmorLight**.h
            - : **ItemEquipment**
            - *weightBehavior* = new **Light**
          - ItemArmorLight.cpp
        - **ItemArmor**.h
          - : **ItemEquipment**
          - *useBehavior* = new **NoUse**
        - ItemArmor.cpp
      - **ItemEquipment**.h
        - : **Item**
      - ItemEquipment.cpp
    - Consumables
      - **ItemConsumable**.h
        - : **Item**
      - ItemConsumable.cpp
    - **Item**.h
      - __*UseBehavior*__ *useBehavior*
      - __*EquipBehavior*__ *equipBehavior*
      - __*WeightBehavior*__ *weightBehavior*
    - Item.cpp

##Content

- Guis
- Managers
  - Objects
  - Audio
- Scenes
- World Objects
  - Blocks
  - Entities
  - Items
    - Weapons
