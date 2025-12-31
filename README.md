name: Reusable Workflow with Input
on:
  workflow_call:
    inputs:
      user_name: # تعريف متغير لاستقبال الاسم
        required: true
        type: string

jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
      - run: echo "مرحباً يا ${{ inputs.user_name }}، تم تشغيل الأكشن بنجاح!"
