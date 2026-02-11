---
name: Central Kitchen Management
description: Design and implement central kitchen systems for food preparation, distribution coordination, and supplier collaboration
---

# Central Kitchen Management Skill

## Purpose

Provide comprehensive central kitchen management system design for businesses operating centralized food preparation facilities serving multiple retail locations, enabling menu planning, production scheduling, quality control, and distribution coordination.

## When to Use This Skill

Use this skill when:
- Client operates central kitchen serving multiple locations
- Centralized food preparation and portioning required
- Recipe standardization and consistency critical
- Distribution to multiple locations needed
- Supplier coordination for bulk ingredients
- Quality control and food safety compliance essential

## Core Components

### 1. Menu Planning and Recipe Management

Centralized menu and recipe management:
- **Menu Item Library**: All menu items with recipes and ingredients
- **Recipe Standardization**: Detailed recipes with exact portions and procedures
- **Ingredient Bill of Materials (BOM)**: Ingredients and quantities per recipe
- **Nutritional Information**: Calculated from ingredient data
- **Allergen Tracking**: Allergen flags for each menu item

**Recipe Structure**:
```
Menu Item: Beef Noodle Soup
Serving Size: 1 bowl (500g)
Yield: 10 servings per batch

Ingredients (BOM):
  - Beef shank: 2kg
  - Noodles (fresh): 1.5kg
  - Broth base: 5L
  - Vegetables (bok choy, scallions): 500g
  - Spices (star anise, ginger, garlic): 200g

Preparation Steps:
  1. Braise beef shank 3 hours
  2. Prepare broth with spices
  3. Portion beef (200g per serving)
  4. Portion noodles (150g per serving)
  5. Assemble: noodles + beef + broth + vegetables

Nutritional (per serving):
  - Calories: 450 kcal
  - Protein: 35g
  - Carbs: 40g
  - Fat: 15g

Allergens: Wheat (noodles), Soy (broth base)
Shelf Life: 3 days refrigerated
```

### 2. Production Planning and Scheduling

Forecast demand and schedule production:
- **Demand Forecasting**: Historical sales data + events + seasonality
- **Production Batches**: Calculate batch sizes and quantities
- **Production Schedule**: Daily/weekly production calendar
- **Equipment Allocation**: Assign equipment (ovens, mixers) to batches
- **Labor Planning**: Staff and skills required for production

**Production Planning Workflow**:
```
Step 1: Demand Forecast
  - Analyze sales data from all locations (past 4 weeks)
  - Adjust for upcoming events, holidays, weather
  - Forecast demand by menu item

Step 2: Calculate Production Needs
  Location 1 (Downtown): Beef Noodle Soup - 50 servings/day
  Location 2 (Airport): Beef Noodle Soup - 40 servings/day
  Location 3 (University): Beef Noodle Soup - 60 servings/day
  Total Demand: 150 servings/day = 15 batches (10 servings/batch)

Step 3: Production Schedule
  Monday:
    - 6am-9am: Prep ingredients (beef, broth)
    - 9am-12pm: Cook batches 1-8 (80 servings)
    - 12pm-3pm: Cook batches 9-15 (70 servings)
    - 3pm-5pm: Portioning and packaging
    - 5pm-6pm: Quality control and labeling

Step 4: Equipment and Labor
  Equipment: 2 large braising pots, 1 industrial stove
  Labor: 1 head chef, 3 prep cooks, 2 packaging staff
```

### 3. Ingredient Procurement and Inventory

Manage ingredient sourcing and inventory:
- **Ingredient Catalog**: All ingredients with suppliers and specs
- **Demand Calculation**: Aggregate ingredient needs across all recipes
- **Supplier Orders**: Auto-calculate order quantities based on production
- **Inventory Tracking**: Real-time ingredient inventory levels
- **Quality Inspection**: Incoming ingredient quality checks

**Procurement Workflow**:
```
Week of March 10-16 Production Plan:
  - Beef Noodle Soup: 1,050 servings (105 batches)
  - Chicken Rice: 800 servings (80 batches)
  - Vegetable Stir-fry: 600 servings (60 batches)

Ingredient Aggregation:
  Beef shank: 105 batches x 2kg = 210kg
  Chicken: 80 batches x 3kg = 240kg
  Fresh vegetables: 165 batches x 2kg = 330kg
  Rice: 80 batches x 5kg = 400kg
  Noodles: 105 batches x 1.5kg = 157.5kg

Supplier Orders (placed Monday for Wednesday delivery):
  - Meat Supplier: Beef 210kg, Chicken 240kg
  - Vegetable Supplier: 330kg mixed vegetables (daily delivery)
  - Dry Goods Supplier: Rice 400kg, Noodles 160kg

Inventory Safety Stock:
  - Meat: 3-day supply (no freezer capacity)
  - Vegetables: 1-day supply (freshness)
  - Dry goods: 2-week supply
```

### 4. Production Execution and Quality Control

Execute production with quality oversight:
- **Production Orders**: Work orders for kitchen staff
- **Batch Tracking**: Track each production batch with batch numbers
- **Quality Checkpoints**: Inspect at critical stages (cooking, portioning)
- **Waste Tracking**: Record waste and reasons
- **Batch Approval**: Head chef approves before distribution

**Production Execution**:
```
Production Order: PO-20260311-001
Menu Item: Beef Noodle Soup
Batch Size: 10 servings
Batches: 15
Assigned: Chef Wang, Prep Team A
Start Time: 6am
Target Completion: 5pm

Quality Checkpoints:
  ✓ Ingredient inspection (6:00am) - Beef quality OK, vegetables fresh
  ✓ Cooking temp check (10:00am) - Broth 95°C (target: 90-100°C)
  ✓ Portioning accuracy (3:30pm) - Sample batch weight 510g (target: 500g ±10g)
  ✓ Taste test (4:00pm) - Approved by Head Chef
  ✓ Final inspection (4:30pm) - Packaging sealed, labels correct

Waste:
  - Beef trimmings: 5kg (2.4% of input)
  - Vegetables (cosmetic reject): 10kg (3.0% of input)
  Total waste: 2.6% (within <5% target)

Batch Numbers: BNS-20260311-001 to BNS-20260311-015
Status: Approved for Distribution
```

### 5. Portioning and Packaging

Standardize portions and packaging:
- **Portion Control**: Exact weights/volumes per serving
- **Packaging Standards**: Containers, sealing, labeling
- **Shelf Life Labeling**: Production date, expiration date
- **Allergen Labeling**: Allergen warnings on packages
- **Batch Traceability**: Batch number on every package

**Portioning Standards**:
```
Menu Item: Beef Noodle Soup
Portion Standard:
  - Noodles: 150g (±5g)
  - Beef: 200g (±10g)
  - Broth: 400ml (±20ml)
  - Vegetables: 50g (±5g)
  Total: 800g (±20g)

Packaging:
  - Container: 1000ml microwave-safe bowl with lid
  - Sealing: Heat-sealed film
  - Label: Menu item, batch number, production date, expiration, allergens
  - Storage: Refrigerated at 0-4°C

Example Label:
  Beef Noodle Soup
  Batch: BNS-20260311-001
  Produced: 2026-03-11 14:30
  Best Before: 2026-03-14
  Store at 0-4°C
  Allergens: Wheat, Soy
  Reheat: Microwave 3 min or steam 5 min
```

### 6. Distribution and Delivery Coordination

Coordinate distribution to retail locations:
- **Distribution Planning**: Determine delivery schedules and routes
- **Inventory Allocation**: Allocate production to locations by demand
- **Temperature Control**: Maintain cold chain during transport
- **Delivery Confirmation**: Track deliveries and exceptions
- **Return and Waste Management**: Handle returns and excess inventory

**Distribution Workflow**:
```
Daily Distribution Schedule (Overnight Delivery):

Production Day: March 11 (complete by 6pm)
Delivery Night: March 11, 10pm - March 12, 4am
Service Day: March 12 (stores open 11am)

Route 1 (North Region): Departs 10pm
  - Location A (Downtown): 150 servings x 5 items = 750 units
  - Location B (University): 120 servings x 5 items = 600 units
  - Location C (Suburban): 80 servings x 5 items = 400 units
  Total: 1,750 units, Vehicle: Refrigerated truck, Arrival: 2am

Route 2 (South Region): Departs 11pm
  - Location D (Airport): 100 servings x 5 items = 500 units
  - Location E (Waterfront): 90 servings x 5 items = 450 units
  Total: 950 units, Vehicle: Refrigerated van, Arrival: 3am

Delivery Confirmation:
  - Driver scans batch labels on delivery
  - Store manager confirms receipt and temp check
  - Any discrepancies logged immediately
  - Central kitchen notified of issues

Temperature Monitoring:
  - Truck interior: 0-4°C maintained
  - Data logger records temp every 5 minutes
  - Alert if temp exceeds 6°C for >15 minutes
```

### 7. Supplier Collaboration

Collaborate with ingredient suppliers:
- **Supplier Portal**: Suppliers receive orders and confirm availability
- **Quality Specifications**: Detailed specs for each ingredient
- **Delivery Scheduling**: Coordinate delivery windows
- **Quality Feedback**: Report quality issues and supplier performance
- **Invoice and Payment**: Automated invoice matching and payment

**Supplier Collaboration System**:
```
Supplier: Fresh Vegetables Co.
Order: Weekly standing order + ad-hoc

Standing Order (Every Monday, Wednesday, Friday):
  - Bok choy: 50kg
  - Scallions: 20kg
  - Carrots: 30kg
  - Delivery: 6am-8am

Quality Specifications:
  - Bok choy: Fresh, no wilting, <5% cosmetic defects
  - Scallions: Green, crisp, uniform size
  - Carrots: Firm, no soft spots, medium size

Supplier Portal Access:
  - View upcoming orders (7-day visibility)
  - Confirm availability or flag shortages
  - Upload quality certificates
  - View payment status

Quality Scorecard (Monthly):
  - On-time delivery: 95% (target: >90%)
  - Quality acceptance: 92% (target: >90%)
  - Order accuracy: 98% (target: >95%)
  Overall: Good Standing
```

### 8. Food Safety and Compliance

Ensure food safety throughout operations:
- **HACCP Compliance**: Implement critical control points
- **Temperature Monitoring**: Log cooking, cooling, storage temps
- **Sanitation Checklists**: Daily cleaning and sanitization
- **Pest Control**: Regular inspections and prevention
- **Audit Trail**: Complete documentation for health inspections

**HACCP Critical Control Points**:
```
CCP 1: Ingredient Receiving
  - Check temperature of refrigerated ingredients (<4°C)
  - Inspect for damage, contamination, pests
  - Record receipt time, temp, supplier, batch

CCP 2: Cooking
  - Minimum internal temp: 75°C for meats
  - Hold time: Minimum 15 seconds at target temp
  - Record batch number, cook time, final temp

CCP 3: Cooling
  - Rapid cooling: 60°C to 20°C within 2 hours
  - Final cooling: 20°C to 4°C within 4 hours
  - Record start time, end time, temps

CCP 4: Storage
  - Refrigeration: 0-4°C continuous
  - Labeling: Production date, expiration date
  - FIFO: First in, first out rotation

CCP 5: Distribution
  - Transport temperature: 0-4°C maintained
  - Delivery time: <4 hours from central kitchen
  - Receiving temp check at retail location
```

## Implementation Checklist

### Requirements Phase
- [ ] Define menu items and recipes
- [ ] Determine production capacity and equipment
- [ ] Identify retail locations and demand patterns
- [ ] Document supplier relationships and sourcing
- [ ] Assess food safety and compliance requirements
- [ ] Define distribution logistics and cold chain needs

### Design Phase
- [ ] Design recipe and BOM structure
- [ ] Model production planning and scheduling
- [ ] Design inventory and procurement workflows
- [ ] Plan quality control checkpoints
- [ ] Design distribution and delivery coordination
- [ ] Plan supplier collaboration interfaces

### Development Phase
- [ ] Build menu and recipe management
- [ ] Implement demand forecasting and production scheduling
- [ ] Develop inventory and supplier order automation
- [ ] Create production execution and quality tracking
- [ ] Build distribution planning and tracking
- [ ] Implement supplier portal and collaboration

### Testing Phase
- [ ] Test recipe scaling and BOM calculations
- [ ] Validate demand forecasting accuracy
- [ ] Test production scheduling with constraints
- [ ] Verify cold chain temperature monitoring
- [ ] User acceptance with production staff and managers
- [ ] Full end-to-end test (planning to delivery)

## Success Metrics

Measure central kitchen system effectiveness:
- **Production Efficiency**: >90% on-time production completion
- **Quality**: <2% waste, >98% quality acceptance at retail
- **Food Safety**: 0 food safety incidents, 100% audit pass rate
- **Inventory Turnover**: 10-15 times/year (fresh ingredients)
- **Distribution**: >98% on-time delivery, 100% temp compliance
- **Cost Control**: Food cost variance <5% vs. standard

## Common Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Demand forecasting inaccuracy | Machine learning on historical data, retail input, buffer stock |
| Production scheduling complexity | Constraint-based scheduling algorithm, manual override |
| Quality consistency across batches | Standardized recipes, training, quality checkpoints |
| Cold chain maintenance | Temperature monitoring, backup refrigeration, fast distribution |
| Supplier reliability | Dual sourcing, quality scorecards, standing orders |
| Retail location inventory management | Real-time visibility, automated reorder triggers |

## Integration Requirements

Central kitchen integrates with:
- **Retail POS Systems**: Sales data for demand forecasting
- **Supplier Systems**: Order placement and confirmations
- **Temperature Sensors**: IoT monitoring for cold chain
- **Distribution Logistics**: Route optimization and tracking
- **Accounting Systems**: Cost tracking and supplier invoices

## Example Input/Output

### Input: Weekly Production Planning Request
```
Week: March 10-16, 2026
Retail Locations: 5 stores
Menu Items: 8 (noodle soups, rice dishes, stir-fries)
Historical Sales: Past 4 weeks data
Upcoming Events: University exam week (higher demand at Location C)
```

### Output: Production Schedule and Ingredient Orders
```
Weekly Production Schedule (March 10-16):

Daily Production (Monday-Saturday):
  Beef Noodle Soup: 150 servings/day = 900 servings/week
  Chicken Rice: 120 servings/day = 720 servings/week
  Vegetable Stir-fry: 100 servings/day = 600 servings/week
  (5 additional items omitted for brevity)

Ingredient Orders (Due Monday):
  Meat Supplier: Beef 1,260kg, Chicken 1,680kg
  Vegetable Supplier: Daily delivery schedule (1,800kg/week)
  Dry Goods: Rice 2,400kg, Noodles 945kg

Production Staffing:
  Monday-Friday: 1 head chef, 4 prep cooks, 3 packaging staff
  Saturday: 1 head chef, 3 prep cooks, 2 packaging staff

Distribution Schedule:
  Daily overnight delivery (10pm-4am) to all 5 locations
  Special: Extra delivery to Location C (University) on Wed/Thu (exam week)

Estimated Costs:
  Ingredients: $15,000
  Labor: $8,000
  Distribution: $2,000
  Total: $25,000
  Cost per serving: $10.42
```

## Version History

- v1.0 (2026-02-11): Initial skill creation for Dimension 7 Industry Experts
