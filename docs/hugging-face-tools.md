# Hugging Face Tools & Capabilities

## Quota System
- GPU operations have a time-based quota (60 seconds per operation)
- Quota resets every ~14 hours
- Basic operations (searches, CPU tasks) are unlimited
- Clear feedback on remaining quota and reset time

## Available Models & Capabilities

### Text Generation
- Access to major models through inference API:
  - Mistral-7B-Instruct-v0.2
  - Zephyr ORPO 141B
  - Gemma-7B
- Models are region-specific (US-based)
- All models support endpoints_compatible tag

### Image Generation
- Access to popular Stable Diffusion models:
  - Stable Diffusion v1.5 (base and inpainting)
  - Stable Diffusion XL Base 1.0
- GPU quota applies (~60s per generation)
- Typical resolution support: 256x256 to 2048x2048

## Usage Guidelines
1. Monitor GPU quota usage (system provides exact feedback)
2. Prioritize CPU operations when possible
3. Plan GPU operations around 14-hour reset cycle
4. Use model search to verify availability before implementation

## Testing Results
- Model searches and browsing don't affect quotas
- GPU operations cost ~60s per significant operation
- Can perform ~24-30 significant GPU operations per day
- System provides precise remaining time until quota reset

## Future Considerations
1. Consider implementing quota monitoring in dashboard
2. Track usage patterns to optimize GPU operation timing
3. Consider backup providers for high-demand periods
4. Monitor for new model additions and capability changes

Note: This document is based on direct testing and verification of the free tier Hugging Face Inference API access. Capabilities may change over time. 