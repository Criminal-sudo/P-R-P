<template>
  <div class="welcome">
    <Row :gutter="[16, 16]">
      <Col :span="18">
        <Card>
          <template #title>
            <span class="title__line">我的常用菜单</span>
          </template>
          <template #extra>
            <SettingFilled />
          </template>
          <div class="address">
            <div class="address-name address-name__jing">
              <span class="name">京</span>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
            </div>
          </div>
          <div class="address">
            <div class="address-name address-name__hu">
              <span class="name">沪</span>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>RTGS当日清算交收情况</Tag>
              </div>
              <div class="tag-item">
                <Tag>预约划款录入</Tag>
              </div>
              <div class="tag-item">
                <Tag>B股资金划拨录入</Tag>
              </div>
              <div class="tag-item">
                <Tag>转融通证券划转查询</Tag>
              </div>
            </div>
          </div>
          <div class="address">
            <div class="address-name address-name__shen">
              <span class="name">深</span>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>当日日终股本查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>董监高历史持有变动凭证</Tag>
              </div>
              <div class="tag-item">
                <Tag>红利派发申报</Tag>
              </div>
            </div>
          </div>
        </Card>
        <Card style="margin-top: 15px">
          <template #title>
            <span class="title__line">历史记录</span>
          </template>
          <div class="address">
            <div class="history-address-name history-address-name__jing">
              <span class="name">京</span>
              <div class="address-name-line"></div>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>股权激励期权初始登记</Tag>
              </div>
              <div class="tag-item">
                <Tag>公司债兑付兑息业务办理</Tag>
              </div>
              <div class="tag-item">
                <Tag>清算结果查询</Tag>
              </div>
            </div>
          </div>
          <div class="address">
            <div class="history-address-name history-address-name__hu">
              <span class="name">沪</span>
              <div class="address-name-line"></div>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>RTGS当日清算交收情况</Tag>
              </div>
              <div class="tag-item">
                <Tag>预约划款录入</Tag>
              </div>
              <div class="tag-item">
                <Tag>B股资金划拨录入</Tag>
              </div>
              <div class="tag-item">
                <Tag>转融通证券划转查询</Tag>
              </div>
            </div>
          </div>
          <div class="address">
            <div class="history-address-name history-address-name__shen">
              <span class="name">深</span>
              <div class="address-name-line"></div>
            </div>
            <div class="tag-group">
              <div class="tag-item">
                <Tag>当日日终股本查询</Tag>
              </div>
              <div class="tag-item">
                <Tag>董监高历史持有变动凭证</Tag>
              </div>
              <div class="tag-item">
                <Tag>红利派发申报</Tag>
              </div>
            </div>
          </div>
        </Card>
      </Col>
      <Col :span="6">
        <Card>
          <div class="current-date-time">
            <span>2021年12月27日 星期一</span>
            <span>下午14:00:00</span>
          </div>
        </Card>
        <Card style="margin-top: 15px">
          <template #title>
            <span class="title__line">连接信息</span>
          </template>
          <div class="connect__status">
            <Avatar size="large" src="https://joeschmoe.io/api/v1/random"></Avatar>
            <div class="connect-tag-group">
              <div class="connect-tag-item">
                <Tag>
                  北京
                  <span class="connect-cricle"></span>
                </Tag>
              </div>
              <div class="connect-tag-item">
                <Tag>
                  上海
                  <span class="no-connect-cricle"></span>
                </Tag>
              </div>
              <div class="connect-tag-item">
                <Tag>
                  深圳
                  <span class="connect-cricle"></span>
                </Tag>
              </div>
            </div>
          </div>
        </Card>
        <Card>
          <template #title>
            <span class="title__line">用户信息</span>
          </template>
          <div class="user-info">
            <Avatar size="large" src="https://joeschmoe.io/api/v1/random" />
            <span class="user-name">管理员 Q54900**</span>
          </div>
          <Space size="large">
            <Tag>
              <span class="user-action-name">修改密码</span>
            </Tag>
            <Tag>
              <span class="user-action-name">权限设置</span>
            </Tag>
            <Tag>
              <span class="user-action-name">配色选择</span>
            </Tag>
          </Space>
        </Card>
        <Card>
          <template #title>
            <span class="title__line">软件信息</span>
          </template>
          <template #extra>
            <span>软件版本：2012012.2.1.5v</span>
          </template>
          <Row :gutter="[16, 16]">
            <Col :span="8">
              <div class="platform">
                <div class="platform-name platform__jing"> 京 </div>
                <div class="platform-business-version"> 业务版本 </div>
                <div class="version"> 211225.0.1.2v </div>
              </div>
            </Col>
            <Col :span="8">
              <div class="platform">
                <div class="platform-name platform__hu"> 沪 </div>
                <div class="platform-business-version"> 业务版本 </div>
                <div class="version"> 211225.0.1.2v </div>
              </div>
            </Col>
            <Col :span="8">
              <div class="platform">
                <div class="platform-name platform__shen"> 深 </div>
                <div class="platform-business-version"> 业务版本 </div>
                <div class="version"> 211225.0.1.2v </div>
              </div>
            </Col>
          </Row>
        </Card>
        <Card>
          <template #title>
            <span class="title__line">证书信息</span>
          </template>
          <div class="veri-info">证书序列号：H0F0400089156524</div>
          <div class="veri-info">用户代码：Q31100**</div>
          <div class="veri-info">证书有效期：2020-06-03 14:49:38 - 2025-06-03 14:49:38</div>
          <div class="veri-info">证书备注：951753</div>
        </Card>
        <Card>
          <template #title>
            <span class="title__line">帮助信息</span>
          </template>
          <Space size="large">
            <Tag>
              <span class="user-action-name">软件手册</span>
            </Tag>
            <Tag>
              <span class="user-action-name">业务手册</span>
            </Tag>
            <Tag>
              <span class="user-action-name">技术指导</span>
            </Tag>
          </Space>
          <img
            style="margin-top: 20px; height: 100px; width: 100%"
            src="~@/assets/images/support.png"
            alt=""
          />
        </Card>
      </Col>
    </Row>
  </div>
</template>

<script lang="ts" setup>
  import { SettingFilled } from '@ant-design/icons-vue';
  import { Card, Tag, Avatar, Row, Col } from 'ant-design-vue';

  defineOptions({
    name: 'DashboardWelcome',
  });
</script>

<style lang="less" scoped>
  @import '@/styles/theme.less';

  // .themeBgColor(welcome);

  .welcome {
    display: flex;
    width: 100%;
    height: calc(100vh - 280px);
    flex-direction: column;

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

    .address {
      width: 100%;

      .address-name__jing {
        background-color: rgba(255, 0, 0, 0.1);

        & .name {
          background-color: rgba(255, 0, 0, 1);
        }
      }

      .address-name__hu {
        background-color: rgba(64, 255, 0, 0.1);

        & .name {
          background-color: rgba(64, 255, 0, 1);
        }
      }

      .address-name__shen {
        background-color: rgba(0, 76, 241, 0.1);

        & .name {
          background-color: rgba(0, 76, 241, 1);
        }
      }

      .history-address-name {
        display: flex;
        justify-items: flex-start;
        align-items: center;
        font-size: 14px;
        font-weight: bold;

        & .name {
          margin-right: 8px !important;
        }
      }

      .history-address-name__jing {
        & .address-name-line {
          background-color: rgba(255, 0, 0, 0.1);
        }

        & .name {
          color: rgba(255, 0, 0, 1) !important;
        }
      }

      .history-address-name__hu {
        & .address-name-line {
          background-color: rgba(64, 255, 0, 0.2);
        }

        & .name {
          color: rgba(64, 255, 0, 1) !important;
        }
      }

      .history-address-name__shen {
        & .address-name-line {
          background-color: rgba(0, 76, 241, 0.2);
        }

        & .name {
          color: rgba(0, 76, 241, 1) !important;
        }
      }

      .address-name-line {
        width: 100%;
        height: 1px !important;
      }

      .address-name {
        width: inherit;
        height: 30px;
        position: relative;
        border-top-left-radius: 20px;
        border-bottom-left-radius: 20px;

        .name {
          position: absolute;
          left: 0;
          top: 50%;
          transform: translateY(-50%);
          width: 30px;
          height: 30px;
          font-size: 14px;
          font-weight: bold;
          border-radius: 50%;
          display: block;
          text-align: center;
          line-height: 30px;
          color: rgba(255, 255, 255, 1);
        }
      }

      .tag-group {
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        padding: 12px 20px;

        & .tag-item {
          flex: 1;
          margin: 0 12px 12px 0;
          width: calc((100% - 60px) / 6);
          min-width: calc((100% - 60px) / 6);
          max-width: calc((100% - 60px) / 6);

          & .ant-tag {
            text-align: center;
            width: 100%;
          }

          &:nth-child(6n) {
            margin-right: 0;
          }
        }
      }
    }

    .current-date-time {
      display: flex;
      justify-content: space-between;
    }

    .connect__status {
      display: flex;

      & .ant-avatar {
        width: 40px;
      }

      & .connect-tag-group {
        flex: 1;
      }
    }

    .connect-tag-group {
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
      padding: 0 0 0 12px;
      align-items: center;

      & .connect-tag-item {
        flex: 1;
        margin: 0 15px 0 0;
        width: calc((100% - 35px) / 3);
        min-width: calc((100% - 35px) / 3);
        max-width: calc((100% - 35px) / 3);

        & .connect-cricle {
          width: 8px;
          height: 8px;
          border-radius: 8px;
          background-color: rgba(255, 0, 0, 1);
          display: inline-block;
          margin-left: 12px;
        }

        & .no-connect-cricle {
          width: 8px;
          height: 8px;
          border-radius: 8px;
          background-color: rgba(153, 153, 153, 1);
          display: inline-block;
          margin-left: 12px;
        }

        & .ant-tag {
          text-align: center;
          width: 100%;
        }

        &:nth-child(3n) {
          margin-right: 0;
        }
      }
    }

    .user-info {
      margin-bottom: 15px;

      .user-name {
        margin-left: 15px;
      }
    }

    .user-action-name {
      color: @primary-color;
    }

    .platform {
      width: 100%;
      height: 140px;
      background-color: rgba(237, 237, 237, 1);
      padding: 30px 15px;

      .platform-name {
        margin: 0 auto 12px auto;
        width: 30px;
        height: 30px;
        text-align: center;
        line-height: 30px;
        border-radius: 30px;
        font-size: 14px;
        font-weight: bold;
        background-color: rgba(255, 0, 0, 1);
        color: rgba(255, 255, 255, 1);
      }

      .platform__jing {
        background-color: rgba(255, 0, 0, 1);
      }

      .platform__hu {
        background-color: rgba(64, 255, 0, 1);
      }

      .platform__shen {
        background-color: rgba(0, 76, 241, 1);
      }

      .platform-business-version,
      .version {
        text-align: center;
      }
    }

    .veri-info {
      width: 100%;
      height: 25px;
      line-height: 25px;
      background-color: rgba(230, 230, 230, 1);
      padding: 0 12px;
      margin-bottom: 10px;
      font-size: 12px;
    }
  }
</style>
