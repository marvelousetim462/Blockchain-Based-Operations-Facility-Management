# Blockchain-Based Operations Facility Management

A comprehensive facility management system built on blockchain technology using Clarity smart contracts. This system provides transparent, immutable, and efficient management of facility operations including space utilization, energy management, maintenance coordination, and cost optimization.

## 🏗️ System Architecture

The system consists of five interconnected smart contracts:

### 1. Facility Manager Verification (`facility-manager-verification.clar`)
- **Purpose**: Validates and manages facility manager credentials
- **Key Features**:
    - Manager verification and certification tracking
    - Role-based access control
    - Credential revocation capabilities
    - Immutable verification history

### 2. Space Utilization (`space-utilization.clar`)
- **Purpose**: Manages facility space allocation and tracking
- **Key Features**:
    - Space creation and capacity management
    - Real-time occupancy tracking
    - Booking system with conflict prevention
    - Utilization analytics and reporting

### 3. Energy Management (`energy-management.clar`)
- **Purpose**: Tracks and optimizes facility energy consumption
- **Key Features**:
    - Smart meter installation and management
    - Energy reading verification system
    - Efficiency calculations and benchmarking
    - Daily consumption tracking and cost analysis

### 4. Maintenance Coordination (`maintenance-coordination.clar`)
- **Purpose**: Coordinates facility maintenance requests and scheduling
- **Key Features**:
    - Maintenance request creation and prioritization
    - Work assignment and status tracking
    - Comprehensive logging system
    - Cost estimation and budget tracking

### 5. Cost Optimization (`cost-optimization.clar`)
- **Purpose**: Analyzes and optimizes facility operational costs
- **Key Features**:
    - Budget allocation and tracking
    - Expense recording and approval workflow
    - Cost savings initiative tracking
    - ROI calculations and financial analytics

## 🚀 Getting Started

### Prerequisites
- Clarity CLI or compatible development environment
- Stacks blockchain testnet access
- Node.js and npm for testing

### Installation

1. Clone the repository:
   \`\`\`bash
   git clone <repository-url>
   cd blockchain-facility-management
   \`\`\`

2. Install dependencies:
   \`\`\`bash
   npm install
   \`\`\`

3. Run tests:
   \`\`\`bash
   npm test
   \`\`\`

### Deployment

Deploy contracts to Stacks testnet:

\`\`\`bash
# Deploy facility manager verification contract
clarinet deploy --testnet contracts/facility-manager-verification.clar

# Deploy other contracts in order
clarinet deploy --testnet contracts/space-utilization.clar
clarinet deploy --testnet contracts/energy-management.clar
clarinet deploy --testnet contracts/maintenance-coordination.clar
clarinet deploy --testnet contracts/cost-optimization.clar
\`\`\`

## 📋 Usage Examples

### Verify a Facility Manager
\`\`\`clarity
(contract-call? .facility-manager-verification verify-manager
'ST2CY5V39NHDPWSXMW9QDT3HC3GD6Q6XX4CFRK9AG
"John Doe"
"Certified Facility Manager (CFM)")
\`\`\`

### Create a Space
\`\`\`clarity
(contract-call? .space-utilization create-space "Conference Room A" u20)
\`\`\`

### Install Energy Meter
\`\`\`clarity
(contract-call? .energy-management install-meter "Building A - Floor 1" "Smart Meter")
\`\`\`

### Create Maintenance Request
\`\`\`clarity
(contract-call? .maintenance-coordination create-request
"Fix HVAC System"
"Air conditioning not working in conference room"
"Building A - Room 101"
u3
u500)
\`\`\`

### Set Budget
\`\`\`clarity
(contract-call? .cost-optimization set-budget "Energy" u202401 u10000)
\`\`\`

## 🧪 Testing

The project includes comprehensive test suites for all contracts using Vitest:

- **Unit Tests**: Test individual contract functions
- **Integration Tests**: Test contract interactions
- **Edge Cases**: Test error conditions and boundary cases

Run specific test suites:
\`\`\`bash
# Test facility manager verification
npm test facility-manager-verification

# Test space utilization
npm test space-utilization

# Test energy management
npm test energy-management

# Test maintenance coordination
npm test maintenance-coordination

# Test cost optimization
npm test cost-optimization
\`\`\`

## 📊 Key Features

### Transparency
- All operations recorded on blockchain
- Immutable audit trail
- Public verification of manager credentials

### Efficiency
- Automated space utilization tracking
- Real-time energy monitoring
- Streamlined maintenance workflows

### Cost Control
- Budget tracking and enforcement
- ROI calculations for improvements
- Expense approval workflows

### Security
- Role-based access control
- Cryptographic verification
- Tamper-proof records

## 🔧 Contract Functions

### Read-Only Functions
- `is-verified-manager`: Check manager verification status
- `get-space-utilization`: Calculate space utilization percentage
- `calculate-efficiency`: Compute energy efficiency metrics
- `calculate-budget-utilization`: Analyze budget usage
- `calculate-roi`: Determine return on investment

### Public Functions
- `verify-manager`: Add verified facility manager
- `create-space`: Register new facility space
- `record-reading`: Log energy consumption data
- `create-request`: Submit maintenance request
- `set-budget`: Allocate departmental budget

## 📈 Analytics and Reporting

The system provides comprehensive analytics:

- **Space Utilization**: Occupancy rates, booking patterns
- **Energy Efficiency**: Consumption trends, cost analysis
- **Maintenance**: Request volumes, completion times
- **Financial**: Budget utilization, cost savings tracking

## 🛡️ Security Considerations

- **Access Control**: Only verified managers can perform critical operations
- **Data Validation**: All inputs validated before processing
- **Error Handling**: Comprehensive error codes and messages
- **Audit Trail**: Complete history of all operations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add tests for new functionality
4. Ensure all tests pass
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation wiki

## 🔄 Version History

- **v1.0.0**: Initial release with core functionality
- **v1.1.0**: Enhanced analytics and reporting
- **v1.2.0**: Improved cost optimization features

---

Built with ❤️ using Clarity and Stacks blockchain technology.
\`\`\`
\`\`\`

Finally, let's create the PR details file:
