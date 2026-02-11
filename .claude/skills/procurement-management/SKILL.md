---
name: Procurement Management
description: Design and implement procurement systems for supplier management, cost analysis, import logistics, and risk assessment
---

# Procurement Management Skill

## Purpose

Provide comprehensive procurement management system design enabling supplier sourcing, RFQ processes, landed cost analysis, import compliance, risk assessment, and procurement workflow automation.

## When to Use This Skill

Use this skill when:
- Client needs supplier sourcing and selection support
- Import logistics and customs compliance required
- Landed cost calculation and comparison essential
- Procurement approval workflows needed
- Supplier performance tracking required
- Risk management for supply chain critical

## Core Components

### 1. Supplier Management

Centralized supplier database and lifecycle management:
- **Supplier Profile**: Company info, certifications, capabilities
- **Supplier Qualification**: Evaluation criteria and approval process
- **Supplier Segmentation**: Strategic, preferred, approved, probationary
- **Supplier Performance Tracking**: Scorecards and KPIs
- **Supplier Relationship Management**: Contracts, contacts, communications

**Supplier Profile Structure**:
```
Supplier: Vietnam Coffee Exports Ltd.
ID: SUP-2026-001
Status: Approved (since 2024-06-15)

Company Information:
  - Location: Ho Chi Minh City, Vietnam
  - Business Type: Exporter, Direct Trade
  - Established: 2010
  - Employees: 50

Capabilities:
  - Products: Green coffee beans (Arabica, Robusta)
  - Certifications: Fair Trade, Organic, Rainforest Alliance
  - Capacity: 500 tons/year
  - MOQ: 500kg per order

Performance (Last 12 Months):
  - Orders: 24
  - On-time delivery: 96%
  - Quality acceptance: 98%
  - Price competitiveness: Good (5-10% below market)
  Overall Score: 4.5/5 (Preferred Supplier)

Contacts:
  - Sales: sales@vietnamcoffee.com
  - Quality: qc@vietnamcoffee.com
  - Logistics: logistics@vietnamcoffee.com
```

### 2. RFQ (Request for Quotation) Process

Systematic supplier quotation and comparison:
- **RFQ Creation**: Define requirements and specifications
- **Supplier Invitation**: Send RFQ to qualified suppliers
- **Quotation Collection**: Receive and standardize quotes
- **Comparison Matrix**: Side-by-side comparison of quotes
- **Supplier Selection**: Evaluate and select winner

**RFQ Workflow**:
```
RFQ: Coffee Roasting Equipment
RFQ ID: RFQ-2026-045
Created: 2026-03-01
Due: 2026-03-15

Requirements:
  - Equipment: Commercial coffee roaster
  - Capacity: 30kg batch size
  - Features: Programmable profiles, smoke reduction
  - Quantity: 2 units
  - Delivery: Taiwan, by April 30, 2026

Invited Suppliers:
  1. Italy Coffee Machines (Italy)
  2. German Roast Tech (Germany)
  3. Taiwan Coffee Equipment (Taiwan)

Received Quotations:
Supplier            | Unit Price | Shipping | Lead Time | Warranty
--------------------|------------|----------|-----------|----------
Italy Coffee        | EUR 15,000 | EUR 800  | 8 weeks   | 2 years
German Roast Tech   | EUR 18,000 | EUR 600  | 6 weeks   | 3 years
Taiwan Coffee Equip | TWD 450,000| TWD 0    | 4 weeks   | 1 year

Evaluation Criteria:
  - Price (40%): Taiwan wins
  - Delivery speed (20%): Taiwan wins
  - Warranty (15%): German wins
  - Brand reputation (15%): Italy wins
  - Local support (10%): Taiwan wins

Selected: Taiwan Coffee Equipment (best overall, local support)
```

### 3. Landed Cost Calculation

Calculate total cost of ownership including all fees:
- **Product Cost**: FOB (Free On Board) or EXW (Ex Works) price
- **Freight Cost**: Air, sea, or land transportation
- **Insurance**: Cargo insurance (typically 1-2% of CIF value)
- **Import Duties and Tariffs**: Based on HS code and origin
- **Customs Clearance Fees**: Broker fees, inspection fees
- **Additional Costs**: Storage, handling, inland transport

**Landed Cost Formula**:
```
Landed Cost = Product Cost (FOB) + Freight + Insurance + Duties + Fees

Example: Coffee Roasting Equipment Import

Product Cost (FOB Taiwan):
  - Unit price: TWD 450,000 x 2 = TWD 900,000

Freight (Domestic):
  - Truck delivery: TWD 5,000

Insurance:
  - Not applicable (domestic purchase)

Import Duties:
  - Not applicable (domestic purchase)

Customs Clearance:
  - Not applicable (domestic purchase)

Additional Costs:
  - Installation: TWD 20,000
  - Training: TWD 10,000

Total Landed Cost: TWD 935,000
Cost per unit: TWD 467,500

Compare to Italy Coffee Machines (imported):
Product Cost (FOB Italy): EUR 15,000 x 2 = EUR 30,000
Freight (Sea): EUR 800
Insurance (1%): EUR 308
CIF Value: EUR 31,108

Import Duties (HS 8419.81, Italy origin, 5%): EUR 1,555
Customs Clearance: TWD 8,000 (EUR 267)
Inland Transport: TWD 6,000 (EUR 200)
Installation: TWD 20,000 (EUR 667)

Total Landed Cost: EUR 33,797 (TWD 1,013,910 @ 30 TWD/EUR)
Cost per unit: TWD 506,955

Savings: TWD 39,455 per unit (7.8%) by choosing Taiwan supplier
```

### 4. Import Compliance and Customs

Ensure compliance with import regulations:
- **HS Code Classification**: Determine correct Harmonized System code
- **Tariff Calculation**: Calculate applicable import duties
- **Import Licenses**: Identify required permits and licenses
- **Documentation**: Prepare commercial invoice, packing list, certificates
- **Customs Clearance**: Coordinate with customs broker

**Import Compliance Checklist**:
```
Import: Green Coffee Beans from Vietnam

Step 1: HS Code Classification
  - Product: Unroasted coffee beans (Arabica)
  - HS Code: 0901.11 (Coffee, not roasted, not decaffeinated)
  - Verification: WCO Harmonized System Database

Step 2: Tariff Rates
  - Taiwan tariff: 5% CIF (for non-FTA countries)
  - Vietnam FTA: Check if applicable (may reduce to 0%)
  - Preferential tariff: Requires Certificate of Origin

Step 3: Import Licenses
  - Food import permit: Required from FDA (Taiwan)
  - Phytosanitary certificate: Required (agricultural product)
  - Certificate of Origin: Required for FTA benefits

Step 4: Documentation
  - Commercial Invoice: Supplier provides
  - Packing List: Supplier provides
  - Bill of Lading: Freight forwarder provides
  - Certificate of Origin: Vietnam Chamber of Commerce
  - Phytosanitary Certificate: Vietnam Ministry of Agriculture
  - Food Import Permit: Apply to Taiwan FDA (7-14 days)

Step 5: Customs Clearance
  - Customs broker: Taiwan Customs Services Ltd.
  - Estimated clearance time: 2-3 days
  - Inspection: Random inspection (20% of shipments)
  - Quarantine: If inspection flagged, add 3-5 days

Total Lead Time: 30 days (order to delivery)
  - Production: 7 days
  - Shipping: 14 days (sea freight)
  - Customs clearance: 3 days
  - Inland transport: 1 day
  - Buffer: 5 days
```

### 5. Cost Analysis and Comparison

Analyze and compare procurement options:
- **Total Cost of Ownership (TCO)**: Include all lifecycle costs
- **Price Benchmarking**: Compare against market prices
- **Volume Discount Analysis**: Calculate break-even for bulk orders
- **Make vs. Buy Analysis**: In-house vs. outsource decision
- **Currency Impact**: Model exchange rate scenarios

**TCO Analysis Example**:
```
Decision: In-house roasting vs. buying roasted coffee

Option A: Buy Green Beans + In-house Roasting
Initial Investment:
  - Roasting equipment: TWD 935,000 (depreciate over 5 years)
  - Training: TWD 50,000 (one-time)

Annual Operating Costs:
  - Green beans: 10,000kg @ TWD 180/kg = TWD 1,800,000
  - Labor (roaster operator): TWD 600,000/year
  - Electricity: TWD 120,000/year
  - Maintenance: TWD 50,000/year
  - Equipment depreciation: TWD 187,000/year
  Total: TWD 2,757,000/year

Cost per kg (roasted): TWD 276

Option B: Buy Pre-Roasted Coffee
Annual Costs:
  - Roasted coffee: 10,000kg @ TWD 360/kg = TWD 3,600,000

Cost per kg (roasted): TWD 360

Comparison (5-year TCO):
Option A: TWD 935,000 (initial) + TWD 2,757,000 x 5 = TWD 14,720,000
Option B: TWD 3,600,000 x 5 = TWD 18,000,000

Savings: TWD 3,280,000 over 5 years (18% lower cost)
Payback Period: 2.1 years

Recommendation: In-house roasting (if volume stable, quality control valued)
```

### 6. Procurement Workflow Automation

Automate procurement processes:
- **Purchase Requisition**: Department requests, approval routing
- **Purchase Order Creation**: Auto-generate PO from approved requisitions
- **Order Tracking**: Monitor PO status from placement to receipt
- **Goods Receipt**: Record and match to PO
- **Invoice Matching**: 3-way match (PO, receipt, invoice)
- **Payment Processing**: Automated payment based on terms

**Procurement Workflow**:
```
Procurement Cycle: Raw Material Ordering

Step 1: Purchase Requisition
  - Requestor: Central Kitchen Manager
  - Item: Beef shank, 500kg
  - Justification: Weekly production needs
  - Estimated Cost: TWD 150,000
  - Approval Required: Operations Director (>TWD 50,000)

Step 2: Approval Routing
  - Automatic routing to Operations Director
  - Email/app notification
  - Approval within 24 hours (SLA)

Step 3: Supplier Selection
  - System recommends approved supplier (based on performance)
  - Procurement creates RFQ if new item or price check needed
  - Select supplier: Preferred Meat Supplier Ltd.

Step 4: Purchase Order Creation
  - Auto-populate from requisition
  - Add delivery terms (NET 30, delivery to central kitchen)
  - PO Number: PO-2026-0311-001
  - Send to supplier via email/portal

Step 5: Order Tracking
  - Supplier confirms order and delivery date
  - System tracks status: Confirmed → Shipped → Delivered
  - Alerts if delivery delayed

Step 6: Goods Receipt
  - Warehouse receives shipment
  - Quality inspection (temp check, visual)
  - Record receipt in system (match to PO)
  - Actual quantity: 500kg (matches PO)

Step 7: Invoice Matching
  - Supplier sends invoice: TWD 152,000
  - System matches: PO (TWD 150,000) vs. Receipt (500kg) vs. Invoice (TWD 152,000)
  - Variance: +TWD 2,000 (1.3%)
  - Escalation: Procurement reviews and approves (market price increase)

Step 8: Payment Processing
  - Payment terms: NET 30 (due April 10)
  - Auto-schedule payment
  - Payment method: Bank transfer
  - Confirmation to supplier
```

### 7. Supplier Performance Management

Track and improve supplier performance:
- **Performance Scorecards**: On-time delivery, quality, price
- **KPI Dashboards**: Trend analysis and benchmarking
- **Issue Tracking**: Log and resolve supplier issues
- **Continuous Improvement**: Feedback and collaboration
- **Supplier Development**: Training and capability building

**Supplier Scorecard**:
```
Supplier: Preferred Meat Supplier Ltd.
Period: Q1 2026 (Jan-Mar)

Metrics:
1. On-Time Delivery: 94% (Target: >95%)
   - Late deliveries: 3 out of 50 orders
   - Root cause: Traffic during holidays
   - Action: Supplier to add buffer time

2. Quality Acceptance: 98% (Target: >95%)
   - Rejections: 1 out of 50 deliveries (temperature issue)
   - Root cause: Refrigeration truck malfunction
   - Action: Supplier upgraded to newer trucks

3. Price Competitiveness: Good (Target: Within 5% of market)
   - Average price: TWD 300/kg
   - Market benchmark: TWD 295/kg (+1.7%)
   - Acceptable variance

4. Responsiveness: Excellent (Target: <4 hours)
   - Average response time: 2 hours
   - Issue resolution time: <24 hours

Overall Score: 4.6/5 (Excellent)
Status: Preferred Supplier (maintain)
Next Review: June 2026
```

### 8. Risk Management

Identify and mitigate procurement risks:
- **Supplier Risk**: Financial stability, operational capacity
- **Geopolitical Risk**: Trade restrictions, tariffs, sanctions
- **Supply Chain Risk**: Disruptions, dependencies, lead times
- **Quality Risk**: Product defects, compliance failures
- **Currency Risk**: Exchange rate fluctuations

**Risk Assessment Framework**:
```
Risk Assessment: Coffee Bean Supplier (Vietnam)

Risk Category 1: Supplier Financial Risk
  - Risk: Supplier bankruptcy or cash flow issues
  - Likelihood: Low (established supplier, good financials)
  - Impact: High (supply disruption)
  - Mitigation: Dual sourcing (add Thailand supplier), shorter payment terms
  - Status: Medium risk (monitor quarterly)

Risk Category 2: Geopolitical Risk
  - Risk: Vietnam trade restrictions or tariff changes
  - Likelihood: Low (stable trade relations)
  - Impact: Medium (increased cost)
  - Mitigation: FTA benefits, alternative sourcing (Colombia)
  - Status: Low risk

Risk Category 3: Supply Chain Risk
  - Risk: Weather disrupts coffee crop or shipping delays
  - Likelihood: Medium (seasonal weather, port congestion)
  - Impact: High (stock-out, higher prices)
  - Mitigation: Safety stock (2-month supply), flexible contracts
  - Status: Medium risk (increase safety stock before rainy season)

Risk Category 4: Quality Risk
  - Risk: Inconsistent coffee quality (batch variation)
  - Likelihood: Medium (agricultural product variability)
  - Impact: Medium (customer complaints, waste)
  - Mitigation: Pre-shipment samples, quality specs, third-party testing
  - Status: Medium risk (quality inspection every batch)

Risk Category 5: Currency Risk
  - Risk: USD/VND exchange rate volatility
  - Likelihood: Medium (emerging market currency)
  - Impact: Medium (±10% cost variance possible)
  - Mitigation: 6-month price lock-in, hedging for large orders
  - Status: Medium risk (lock pricing for Q2 orders)

Overall Procurement Risk: MEDIUM
Recommendation: Proceed with diversification (add second supplier)
```

## Implementation Checklist

### Requirements Phase
- [ ] Identify procurement categories and spend
- [ ] Define supplier qualification criteria
- [ ] Document import/export requirements
- [ ] Determine approval workflows and thresholds
- [ ] Assess risk management needs
- [ ] Define performance tracking metrics

### Design Phase
- [ ] Design supplier management database
- [ ] Model RFQ and quotation comparison
- [ ] Design landed cost calculator
- [ ] Plan import compliance workflows
- [ ] Design procurement workflow automation
- [ ] Define supplier scorecard structure

### Development Phase
- [ ] Build supplier portal and database
- [ ] Implement RFQ and comparison tools
- [ ] Develop landed cost calculator
- [ ] Build import documentation and tracking
- [ ] Automate procurement workflows
- [ ] Create supplier performance dashboards

### Testing Phase
- [ ] Test landed cost calculations (accuracy <1%)
- [ ] Validate import compliance (HS codes, tariffs)
- [ ] Test procurement workflows (requisition to payment)
- [ ] Verify supplier performance tracking
- [ ] User acceptance with procurement team
- [ ] Integration testing (ERP, accounting, inventory)

## Success Metrics

Measure procurement system effectiveness:
- **Cost Savings**: 5-10% procurement cost reduction
- **Cycle Time**: 30% reduction in requisition-to-PO time
- **Supplier Performance**: >95% on-time delivery, >98% quality
- **Compliance**: 100% import compliance, 0 customs issues
- **Spend Visibility**: >90% spend managed in system
- **Risk Mitigation**: 0 major supply disruptions

## Common Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Supplier data quality | Mandatory fields, regular updates, supplier self-service portal |
| Complex landed cost calculations | Automated calculator, template-based, validation rules |
| Import compliance complexity | HS code lookup tool, customs broker integration, checklists |
| Procurement maverick spending | Enforce approval workflows, preferred supplier catalogs |
| Supplier performance tracking burden | Automated data collection from PO/receipt, exception reporting |
| Currency volatility | Price lock-ins, hedging strategies, multi-currency support |

## Integration Requirements

Procurement integrates with:
- **ERP Systems**: Inventory, accounting, financials
- **Supplier Systems**: Electronic ordering, invoicing
- **Customs Systems**: Import declaration, duty calculation
- **Banking Systems**: Payment processing, FX rates
- **Quality Systems**: Inspection results, certifications

## Example Input/Output

### Input: Supplier Selection Request
```
Request: Select coffee bean supplier for 12,000kg annual volume
Requirements:
  - Product: Arabica green beans, specialty grade
  - Certifications: Fair Trade or Direct Trade
  - Delivery: Monthly shipments (1,000kg each)
  - Budget: TWD 200-250/kg landed cost
  - Lead time: <45 days
```

### Output: Supplier Recommendation
```
Recommendation: Vietnam Coffee Exports Ltd.

Landed Cost Analysis:
  FOB Price: USD 4.50/kg (TWD 135/kg @ 30 TWD/USD)
  Freight (sea): USD 0.30/kg (TWD 9/kg)
  Insurance: USD 0.05/kg (TWD 1.5/kg)
  Tariff (0% - FTA): USD 0/kg
  Customs clearance: TWD 0.50/kg
  Inland transport: TWD 2/kg
  Total Landed Cost: TWD 148/kg (within budget)

Performance Record:
  - 2-year partnership: 24 deliveries, 96% on-time
  - Quality: 98% acceptance rate
  - Certifications: Fair Trade, Organic, Rainforest Alliance
  - Capacity: Sufficient for 12,000kg/year
  - Lead time: 30-40 days (within requirement)

Risk Assessment: MEDIUM-LOW
  - Dual sourcing recommended (add Colombia supplier for 30% volume)
  - Safety stock: 2-month supply (2,000kg)

Contract Terms:
  - Price: USD 4.50/kg (lock for 6 months, review quarterly)
  - Payment: NET 30 (after delivery and quality check)
  - Delivery: Monthly shipments, 1,000kg each
  - Quality: Pre-shipment sample required, third-party testing

Estimated Annual Cost: TWD 1,776,000 (12,000kg @ TWD 148/kg)
Savings: TWD 624,000 vs. buying roasted coffee locally
```

## Version History

- v1.0 (2026-02-11): Initial skill creation for Dimension 7 Industry Experts
