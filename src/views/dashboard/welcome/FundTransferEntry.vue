<template>
  <div class="fund-transfer-entry">
    <Card class="form-group--card">
      <Form
        :model="formState"
        name="fund-transfer-entry-form"
        layout="vertical"
        autocomplete="off"
        @finish="onFinish"
        @finish-failed="onFinishFailed"
      >
        <Row :gutter="24">
          <Col :span="8">
            <Form.Item label="申报日期：">
              <DatePicker v-model="formState.declarationDate" style="width: 100%"></DatePicker>
            </Form.Item>
          </Col>
        </Row>
        <div class="form-title">
          <span class="title">付款人信息</span>
          <span class="line"></span>
        </div>
        <Row :gutter="24">
          <Col :span="8">
            <Form.Item label="付款方账号：">
              <Select
                v-model="formState.payerAccount"
                :options="[]"
                placeholder="请选择付款方账号"
              />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="付款方银行代码：">
              <Select
                v-model="formState.payerBankCode"
                :options="[]"
                placeholder="请选择付款方银行代码"
              />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="付款方名称：">
              <Select v-model="formState.payerName" :options="[]" placeholder="请选择付款方名称" />
            </Form.Item>
          </Col>
        </Row>
        <div class="form-title">
          <span class="title">收款人信息</span>
          <span class="line"></span>
        </div>
        <Row :gutter="24">
          <Col :span="8">
            <Form.Item label="收款方账号：">
              <Select
                v-model="formState.payeeAccount"
                :options="[]"
                placeholder="请选择收款方账号"
              />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="收款方银行代码：">
              <Select
                v-model="formState.payeeBankCode"
                :options="[]"
                placeholder="请选择收款方银行代码"
              />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="收款方名称：">
              <Select v-model="formState.payeeName" :options="[]" placeholder="请选择收款方名称" />
            </Form.Item>
          </Col>
        </Row>
        <div class="form-title">
          <span class="title">划款详情</span>
          <span class="line"></span>
        </div>
        <Row :gutter="24">
          <Col :span="8">
            <Form.Item label="划款金额：">
              <Input v-model="formState.transferAmount" placeholder="请输入划款金额" />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="币种：">
              <Select v-model="formState.currency" :options="[]" placeholder="请选择币种" />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="当前可用：">
              <Select
                v-model="formState.currentlyAvailable"
                :options="[]"
                placeholder="请输入当前可用"
              />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="划款金额：">
              <Input v-model="formState.convertTransferAmount" placeholder="请输入划款金额" />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="划款用途：">
              <Select v-model="formState.transferUse" :options="[]" placeholder="请选择划款用途" />
            </Form.Item>
          </Col>
          <Col :span="8">
            <Form.Item label="摘要：">
              <Select v-model="formState.summary" :options="[]" placeholder="请输入摘要" />
            </Form.Item>
          </Col>
        </Row>
      </Form>
      <template #actions>
        <div class="submit">
          <Space :size="25">
            <Button type="primary">录入</Button>
            <Button>删除</Button>
            <Button>置空</Button>
          </Space>
        </div>
      </template>
    </Card>
    <Card>
      <template #title>
        <span class="title__line">交易记录</span>
      </template>
      <template #extra>
        <Space :size="12">
          <Loading3QuartersOutlined />
          <FunnelPlotOutlined />
        </Space>
      </template>
      <Table :columns="columns" :data-source="data" />
    </Card>
  </div>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';
  import { Loading3QuartersOutlined, FunnelPlotOutlined } from '@ant-design/icons-vue';
  import {
    Row,
    Col,
    Card,
    Form,
    DatePicker,
    Select,
    Input,
    Button,
    Space,
    Table,
  } from 'ant-design-vue';

  interface FormState {
    declarationDate: Date | string;
    payerAccount: string | number;
    payerBankCode: string | number;
    payerName: string | number;
    payeeAccount: string | number;
    payeeBankCode: string | number;
    payeeName: string | number;
    transferAmount: string | number;
    currency: string | number;
    currentlyAvailable: string | number;
    convertTransferAmount: string | number;
    transferUse: string | number;
    summary: string | number;
  }

  defineOptions({
    name: 'DashboardFundTransferEntry',
  });

  const formState = reactive<FormState>({
    declarationDate: '',
    payerAccount: '',
    payerBankCode: '',
    payerName: '',
    payeeAccount: '',
    payeeBankCode: '',
    payeeName: '',
    transferAmount: '',
    currency: '',
    currentlyAvailable: '',
    convertTransferAmount: '',
    transferUse: '',
    summary: '',
  });

  const onFinish = (values: any) => {
    console.log('Success：', values);
  };

  const onFinishFailed = (errirInfo: any) => {
    console.log('Failed：', errirInfo);
  };

  const columns = [
    {
      title: '序号',
      dataIndex: 'serial',
      key: 'serial',
    },
    {
      title: '复核授权状态',
      dataIndex: 'status',
      key: 'status',
    },
    {
      title: '金额',
      dataIndex: 'amount',
      key: 'amount',
    },
    {
      title: '付款方资金账户',
      dataIndex: 'payerAccount',
      key: 'payerAccount',
    },
    {
      title: '付款方名称',
      dataIndex: 'payerName',
      key: 'payerName',
    },
    {
      title: '收款方资金账户',
      dataIndex: 'payeeAccount',
      key: 'payeeAccount',
    },
    {
      title: '收款方名称',
      dataIndex: 'payeeName',
      key: 'payeeName',
    },
    {
      title: '币种',
      dataIndex: 'currency',
      key: 'currency',
    },
    {
      title: '摘要',
      dataIndex: 'summary',
      key: 'summary',
    },
    {
      title: '申报日期',
      dataIndex: 'declarationDate',
      key: 'declarationDate',
    },
    {
      title: '付款方银行代码',
      dataIndex: 'payerBankCode',
      key: 'payerBankCode',
    },
    {
      title: '收款方银行代码',
      dataIndex: 'payeeBankCode',
      key: 'payeeBankCode',
    },
    {
      title: '受理编号',
      dataIndex: 'acceptanceNumber',
      key: 'acceptanceNumber',
    },
    {
      title: '受理日期',
      dataIndex: 'acceptanceDate',
      key: 'acceptanceDate',
    },
    {
      title: '受理时间',
      dataIndex: 'declarationTime',
      key: 'declarationTime',
    },
    {
      title: '录入操作员',
      dataIndex: 'operator',
      key: 'operator',
    },
  ];

  const data = [];
</script>

<style lang="less" scoped>
  .form-title {
    display: flex;
    align-items: center;
    margin-bottom: 15px;

    & > .title {
      color: @primary-color;
      font-size: 14px;
      font-weight: 600;
      margin-right: 10px;
    }

    & > .line {
      display: inline-block;
      flex: 1;
      height: 6px;
      background-color: rgba(239, 239, 239, 1);
    }
  }

  .form-group--card {
    /deep/ .ant-card-actions > li {
      margin: 0 !important;
    }

    .submit {
      width: 100%;
      height: 65px;
      line-height: 65px;
      background-color: rgba(245, 245, 245, 1);
    }
  }

  .title__line {
    &::before {
      content: ' ';
      display: inline-block;
      width: 4px;
      height: 14px;
      background-color: @primary-color;
      vertical-align: middle;
      margin-right: 8px;
    }
  }
</style>
